.. _curve-overview:


==================
Curve: Overview
==================

This document provides an overview of Curve aimed at a technical audience.  This document assumes a basic familiarity with the Ethereum blockchain and smart contracts.  We will introduce the major concepts of Curve with a focus on the technical specifications.

If you are not technical we recommend visiting the [Curve Documentation](https://resources.curve.fi/).



Curve Liquidity Pools
=====================

Curve maintains several dozen non-custodial **liquidity pools**.  Each liquidity pool is an Ethereum smart contract that accepts deposits in two or more specific denominations of tokens.  The tokens in most liquidity pools are expected to hold equivalent values.  For example, exchanging a USDT dollarcoin for one USDC dollarcoin will be an equal exchange of value if both coins maintain a 1:1 peg to the US Dollar.

Users who **"provide liquidity"** (deposit tokens) into Curve liquidity pools are permitted to withdraw this value in any of the tokens denominated by the pool.  Depositing $1000 into the [Y Pool](https://www.curve.fi/3pool) would permit the user to withdraw $1000 in the three denominations the pool accepts, USDT, USDC, and DAI.

Each liquidity pool is considered to be **"balanced"** if it contains a balance of tokens in similar proportion.  If a massive run occurs on one of the coins in the pool, it may be presumed that this coin has increased in value relative to other coins in the pool.  Curve liquidity pools contain a built-in **Automated Market Maker (AMM)** that automatically adjusts the **relative price** of each coin based on the current supply.  Curve is unique among liquidity pools in using a formula that combines a linear invariant and a constant-product invariant that provides more stability.  This formula is described in detail in the [Curve White Paper](https://www.curve.fi/stableswap-paper.pdf).  

![Balanced Liquidity Pool](/images/1-Balanced-Liquidity-Pool.png)
Figure 1: Balanced Liquidity Pool

The smart contract logic within each liquidity pool automatically calculates an **implied price** of the tokens based on the current balance within the pool.  Users withdraw from the pool at the implied price of the tokens.

A listing of all available pools is contained in the Registry.  The full technical details of the registry are [available here](/registry-overview.rst).


MetaPools
=====================
Several Curve liquidity pools are referred to as **Metapools**.  Metapools are liquidity pools that trade between one token and another liquidity pool.  The underlying pool in a metapool is often referred to as a **base pool**.  Within a metapool, users can trade directly between tokens in the metapool and the base pool.  


![Balanced Metapool](/images/2-Balanced-Metapool.png)
Figure 2: Balanced Metapool

Common base pools include:

 * [**3Pool** (dollar):](https://curve.fi/3pool) _Contains [DAI](https://etherscan.io/address/0x6B175474E89094C44Da98b954EedeAC495271d0F), [USDC](https://etherscan.io/address/0xA0b86991c6218b36c1d19D4a2e9Eb0cE3606eB48), and [USDT](https://etherscan.io/address/0xdAC17F958D2ee523a2206206994597C13D831ec7)_
 * [**sBTC** (bitcoin):](https://curve.fi/sbtc) _Contains [renBTC](https://etherscan.io/address/0xEB4C2781e4ebA804CE9a9803C67d0893436bB27D), [wBTC](https://etherscan.io/address/0x2260FAC5E5542a773Aa44fBCfeDf7C193bc2C599), [sBTC](https://etherscan.io/address/0xfE18be6b3Bd88A2D2A7f928d00292E7a9963CfC6)_

For example, in the GUSD metapool [GUSD, [3Pool]], users can trade between GUSD and the tokens in 3Pool (DAI, USDC, USDT) allowing for four total tokens.


$CRV, veCRV and Fee Distribution
=====================
The **[$CRV token](https://etherscan.io/token/0xD533a949740bb3306d119CC777fa900bA034cd52)** is the governance token for activity around the Curve site.  There will be a total of 3.03 billion $CRV, with details about the supply described on the [Curve Tokenomics page](https://resources.curve.fi/base-features/understanding-tokenomics).  Users who provide liquidity (aka **liquidity providers**) receive a distribution of $CRV every week.

Curve levies a 0.04% fee on all transactions within a pool.  Half of these fees are distributed to liquidity providers, the other half are distributed to users who have staked the $CRV token.

The primary action that can be taken with $CRV is to lock Curve for a time period between 1-4 years.  Locking $CRV entitles holders to receive a portion of trading fees, described below.  Additionally, $CRV provides users with a valueless token called **vote escrowed CRV (veCRV)**.  The amount of veCRV earned by locking $CRV increases linearly with the duration of the lock, ranging from 0.25 veCRV for a 1 year lock to 1.00 veCRV for a 4 year lock.  

![$CRV Locking](/images/3-Curve-Locking.png)
Figure 3: $CRV Locking

There are two key purposes of veCRV
 * Boost rewards for liquidity providers (described below)
 * Submit and vote on proposals listed in the [governance forum](https://gov.curve.fi).  

Additional information on veCRV can be found in [Curve's resource page](https://resources.curve.fi/base-features/understanding-voting).


Cross Asset Swaps
=====================
In 2021, Curve introduced the capability to swap between two different assets.  The feature is [documented here](/cross-asset-swaps.rst).


Public Functions
=====================
All Curve liquidity pools contain the following public functions:

## Mutative

>**add_liquidity(amount, min_mint_amount)**<br>
>_Deposit funds into the liquidity pool_
> * amounts _uint256[number of coins in pool]_: Amount of tokens
> * min_mint_amount _uint256_: Minimum acceptable mint to protect against slippage

>**remove_liquidity(_amount, min_amounts)**<br>
>_Withdraw funds proportionally from the liquidity pool_
> * _amount _uint256_: Amount of tokens
> * _min_amounts _uint256[number of coins in pool]_: Minimum acceptable mint to protect against slippage
> * _Logs a RemoveLiquidity event_

>**remove_liquidity_imbalance(amounts, max_burn_amount)**<br>
>_Withdraw funds disproportionatelyfrom the liquidity pool_
> * amounts _uint256_[number of coins in pool]: Balances to withdraw from each denomination
> * max_burn_amount _uint256_: Revert if token amount is greater than this value, to protect against slippage
> * _Logs a RemoveLiquidity event_

>**remove_liquidity_one_coin(_token_amount, i, min_amount)**<br>
>_Withdraw _token_amount liquidity in the form of coin i_
> * _token_amount _uint256_: Amount of liquidity to remove
> * i _uint256_: Index of coin to withdraw 
> * min_amount _uint256_: Revert token amount is less than this value, to protect against slippage
> * _Logs a RemoveLiquidityOne event_

>**exchange(i, j, dx, min_dy)**<br>
>_Exchange dx number of i coins for j coins without providing liquidity_
> * i _uint256_: Index of first coin
> * j _uint256_: Index of second coin
> * dx _uint256_: Amount of coins to exchange
> * min_dy _uint256_: Revert if transaction is less than this value
> * _Logs a TokenExchange event_


## Constant
>**calc_token_amount(amounts, deposit)**<br>
>_Simple method for calculating change in token supply on deposit or withdrawal.<br>
>Does not consider fees, so not useful for precise calculations._
> * amounts _uint256[number of coins in pool]_: Number of coins deposited or withdrawn
> * deposit _bool_: True if deposit, False if withdrawal
> * returns _uint256_: Calculated token amount

>**get_virtual_price()**<br>
>_Returns portfolio virtual price (for calculating profit)_
> * returns _uint256_: Price, scaled by 1e18

>**get_dy(i, j, dx)**<br>
>_Returns the number of j coins received for exchanging dx number of i coins in c-units_
> * i _uint256_: index of first coin
> * j _uint256_: index of second coin
> * dx _uint256_: amount of coins to exchange
> * returns: number of coins received (after fee)

>**get_dy_underlying(i, j, dx)**<br>
>_Returns the number of j coins received for exchanging dx number of i coins in underlying units_
> * i _uint256_: index of first coin
> * j _uint256_: index of second coin
> * dx _uint256_: amount of coins to exchange
> * returns: number of coins received (after fee)



Owner Functions
=====================
The following functions exist only for the deployer of the contract.  They are not documented in full detail here, but provided for further understanding of the capabilities reserved for pool admins.

 * **ramp_A:** Create a linear ramp to adjust the **"Amplification" parameter (A)**, as described in the white paper.  Logs a RampA event.
 * **stop_ramp_A:** End an active ramp and sets the value of A at the current value.  Logs a StopRampA event.
 * **commit_new_fee:** Set a new admin fee to take effect after a future time for the pool.  Logs a CommitNewFee event.
 * **apply_new_fee:** Immediately begin the new fee.  Logs a NewFee event.
 * **commit_transfer_ownership:** Assign a new admin to take over the contract at a future date.  Logs a CommitNewAdmin event.
 * **apply_transfer_ownership:** Execute the transfer of ownership of the contract.  Logs a NewAdmin event.
 * **revert_new_parameters:** Revert a new fee 
 * **revert_transfer_ownership:** Revert an ownership transfer
 * **withdraw_admin_fees:** Transfer admin fees to the admin
 * **kill_me:** Halt the contract
 * **unkill_me:** Revive the contract


