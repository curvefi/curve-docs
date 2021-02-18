.. _addresses-overview:

=========
Addresses
=========

Here is a list of all current contract deployments within the Curve protocol.

Mainnet Contracts
=================


Base Pools
----------

Base pools in Curve contain two or more tokens and implement the  `Curve stable swap exchange mechanism <https://www.curve.fi/stableswap-paper.pdf>`_. Note that for a single base or meta pool there are multiple deployed contracts, which are of the following formats:

- ``StableSwap<pool>.vy``: Curve stablecoin AMM contract
- ``Deposit<pool>.vy``: contract used to wrap underlying tokens prior to depositing them into the pool (not always required)
- ``CurveContract<version>.vy``: LP token contract for the pool

Here is a list of all base pool contracts currently in use: 

.. csv-table::
   :header: "Pool", "Source", "Address"

   3Pool, `StableSwap3Pool.vy <https://github.com/curvefi/curve-contract/blob/master/contracts/pools/3pool/StableSwap3Pool.vy>`_, `0xbEbc44782C7dB0a1A60Cb6fe97d0b483032FF1C7 <https://etherscan.io/address/0xbebc44782c7db0a1a60cb6fe97d0b483032ff1c7#code>`_
   3Pool, `CurveTokenV2.vy <https://github.com/curvefi/curve-contract/blob/master/contracts/tokens/CurveTokenV2.vy>`_, `0x6c3F90f043a72FA612cbac8115EE7e52BDe6E490 <https://etherscan.io/address/0x6c3F90f043a72FA612cbac8115EE7e52BDe6E490#code>`_
   AAVE, `CurveTokenV3.vy <https://github.com/curvefi/curve-contract/blob/master/contracts/tokens/CurveTokenV3.vy>`_, `0xFd2a8fA60Abd58Efe3EeE34dd494cD491dC14900 <https://etherscan.io/address/0xFd2a8fA60Abd58Efe3EeE34dd494cD491dC14900#code>`_
   AAVE, `StableSwapAave.vy <https://github.com/curvefi/curve-contract/blob/master/contracts/pools/aave/StableSwapAave.vy>`_, `0xDeBF20617708857ebe4F679508E7b7863a8A8EeE <https://etherscan.io/address/0xDeBF20617708857ebe4F679508E7b7863a8A8EeE#code>`_
   ankrETH, `StableSwapAETH.vy <https://github.com/curvefi/curve-contract/blob/master/contracts/pools/aeth/StableSwapAETH.vy>`_, `0xA96A65c051bF88B4095Ee1f2451C2A9d43F53Ae2 <https://etherscan.io/address/0xA96A65c051bF88B4095Ee1f2451C2A9d43F53Ae2#code>`_
   ankrETH, `CurveTokenV3.vy <https://github.com/curvefi/curve-contract/blob/master/contracts/tokens/CurveTokenV3.vy>`_, `0xaA17A236F2bAdc98DDc0Cf999AbB47D47Fc0A6Cf <https://etherscan.io/address/0xaA17A236F2bAdc98DDc0Cf999AbB47D47Fc0A6Cf#code>`_
   BUSD, `StableSwapBUSD.vy <https://github.com/curvefi/curve-contract/blob/master/contracts/pools/busd/StableSwapBUSD.vy>`_, `0x79a8C46DeA5aDa233ABaFFD40F3A0A2B1e5A4F27 <https://etherscan.io/address/0x79a8C46DeA5aDa233ABaFFD40F3A0A2B1e5A4F27#code>`_
   BUSD, `DepositBUSD.vy <https://github.com/curvefi/curve-contract/blob/master/contracts/pools/busd/DepositBUSD.vy>`_, `0xb6c057591E073249F2D9D88Ba59a46CFC9B59EdB <https://etherscan.io/address/0xb6c057591e073249f2d9d88ba59a46cfc9b59edb#code>`_
   BUSD, `CurveTokenV1.vy <https://github.com/curvefi/curve-contract/blob/master/contracts/tokens/CurveTokenV1.vy>`_, `0x3B3Ac5386837Dc563660FB6a0937DFAa5924333B <https://etherscan.io/address/0x3B3Ac5386837Dc563660FB6a0937DFAa5924333B#code>`_
   Compound, `StableSwapCompound.vy <https://github.com/curvefi/curve-contract/blob/master/contracts/pools/compound/StableSwapCompound.vy>`_, `0xA2B47E3D5c44877cca798226B7B8118F9BFb7A56 <https://etherscan.io/address/0xA2B47E3D5c44877cca798226B7B8118F9BFb7A56#code>`_
   Compound, `DepositCompound.vy <https://github.com/curvefi/curve-contract/blob/master/contracts/pools/compound/DepositCompound.vy>`_, `0xeB21209ae4C2c9FF2a86ACA31E123764A3B6Bc06 <https://etherscan.io/address/0xeb21209ae4c2c9ff2a86aca31e123764a3b6bc06#code>`_
   Compound, `CurveContractV1.vy <https://github.com/curvefi/curve-contract/blob/master/contracts/tokens/CurveTokenV1.vy>`_, `0x845838DF265Dcd2c412A1Dc9e959c7d08537f8a2 <https://etherscan.io/address/0x845838DF265Dcd2c412A1Dc9e959c7d08537f8a2#code>`_
   EURS, `StableSwapEURS.vy <https://github.com/curvefi/curve-contract/blob/master/contracts/pools/eurs/StableSwapEURS.vy>`_, `0x0Ce6a5fF5217e38315f87032CF90686C96627CAA <https://etherscan.io/address/0x0Ce6a5fF5217e38315f87032CF90686C96627CAA#code>`_
   EURS, `CurveTokenV3.vy <https://github.com/curvefi/curve-contract/blob/master/contracts/tokens/CurveTokenV3.vy>`_, `0x194eBd173F6cDacE046C53eACcE9B953F28411d1 <https://etherscan.io/address/0x194eBd173F6cDacE046C53eACcE9B953F28411d1#code>`_
   hBTC, `StableSwapHBTC.vy <https://github.com/curvefi/curve-contract/blob/master/contracts/pools/hbtc/StableSwapHBTC.vy>`_, `0x4CA9b3063Ec5866A4B82E437059D2C43d1be596F <https://etherscan.io/address/0x4CA9b3063Ec5866A4B82E437059D2C43d1be596F#code>`_
   hBTC, `CurveTokenV2.vy <https://github.com/curvefi/curve-contract/blob/master/contracts/tokens/CurveTokenV2.vy>`_, `0xb19059ebb43466C323583928285a49f558E572Fd <https://etherscan.io/address/0xb19059ebb43466C323583928285a49f558E572Fd#code>`_
   PAX, `DepositPax.vy <https://github.com/curvefi/curve-contract/blob/master/contracts/pools/pax/DepositPax.vy>`_, `0xA50cCc70b6a011CffDdf45057E39679379187287 <https://etherscan.io/address/0xa50ccc70b6a011cffddf45057e39679379187287#code>`_
   PAX, `StableSwapPax.vy <https://github.com/curvefi/curve-contract/blob/master/contracts/pools/pax/StableSwapPax.vy>`_, `0x06364f10B501e868329afBc005b3492902d6C763 <https://etherscan.io/address/0x06364f10B501e868329afBc005b3492902d6C763#code>`_
   PAX, `CurveTokenV1.vy <https://github.com/curvefi/curve-contract/blob/master/contracts/tokens/CurveTokenV1.vy>`_, `0xD905e2eaeBe188fc92179b6350807D8bd91Db0D8 <https://etherscan.io/address/0xD905e2eaeBe188fc92179b6350807D8bd91Db0D8#code>`_
   renBTC, `StableSwapRen.vy <https://github.com/curvefi/curve-contract/blob/master/contracts/pools/ren/StableSwapRen.vy>`_, `0x93054188d876f558f4a66B2EF1d97d16eDf0895B <https://etherscan.io/address/0x93054188d876f558f4a66B2EF1d97d16eDf0895B#code>`_
   renBTC, `CurveTokenV1.vy <https://github.com/curvefi/curve-contract/blob/master/contracts/tokens/CurveTokenV1.vy>`_, `0x49849C98ae39Fff122806C06791Fa73784FB3675 <https://etherscan.io/address/0x49849C98ae39Fff122806C06791Fa73784FB3675#code>`_
   sAAVE, `StableSwapSAAVE.vy <https://github.com/curvefi/curve-contract/blob/master/contracts/pools/saave/StableSwapSAAVE.vy>`_, `0xEB16Ae0052ed37f479f7fe63849198Df1765a733 <https://etherscan.io/address/0xeb16ae0052ed37f479f7fe63849198df1765a733#code>`_
   sAAVE, `CurveTokenV3.vy <https://github.com/curvefi/curve-contract/blob/master/contracts/tokens/CurveTokenV3.vy>`_, `0x02d341CcB60fAaf662bC0554d13778015d1b285C <https://etherscan.io/address/0x02d341CcB60fAaf662bC0554d13778015d1b285C#code>`_
   sBTC, `StableSwapSBTC.vy <https://github.com/curvefi/curve-contract/blob/master/contracts/pools/sbtc/StableSwapSBTC.vy>`_, `0x7fC77b5c7614E1533320Ea6DDc2Eb61fa00A9714 <https://etherscan.io/address/0x7fC77b5c7614E1533320Ea6DDc2Eb61fa00A9714#code>`_ 
   sBTC, `CurveTokenV1.vy <https://github.com/curvefi/curve-contract/blob/master/contracts/tokens/CurveTokenV1.vy>`_, `0x075b1bb99792c9E1041bA13afEf80C91a1e70fB3 <https://etherscan.io/address/0x075b1bb99792c9E1041bA13afEf80C91a1e70fB3#code>`_
   sETH, `StableSwapSETH.vy <https://github.com/curvefi/curve-contract/blob/master/contracts/pools/seth/StableSwapSETH.vy>`_, `0xc5424B857f758E906013F3555Dad202e4bdB4567 <https://etherscan.io/address/0xc5424b857f758e906013f3555dad202e4bdb4567#code>`_
   sETH, `CurveTokenV3.vy <https://github.com/curvefi/curve-contract/blob/master/contracts/tokens/CurveTokenV3.vy>`_, `0xA3D87FffcE63B53E0d54fAa1cc983B7eB0b74A9c <https://etherscan.io/address/0xA3D87FffcE63B53E0d54fAa1cc983B7eB0b74A9c#code>`_
   stETH, `StableSwapSTETH.vy <https://github.com/curvefi/curve-contract/blob/master/contracts/pools/steth/StableSwapSTETH.vy>`_, `0xDC24316b9AE028F1497c275EB9192a3Ea0f67022 <https://etherscan.io/address/0xDC24316b9AE028F1497c275EB9192a3Ea0f67022#code>`_
   stETH, `CurveTokenV3.vy <https://github.com/curvefi/curve-contract/blob/master/contracts/tokens/CurveTokenV3.vy>`_, `0x06325440D014e39736583c165C2963BA99fAf14E <https://etherscan.io/address/0x06325440D014e39736583c165C2963BA99fAf14E#code>`_
   sUSD, `DepositSUSD.vy <https://github.com/curvefi/curve-contract/blob/master/contracts/pools/susd/DepositSUSD.vy>`_, `0xFCBa3E75865d2d561BE8D220616520c171F12851 <https://etherscan.io/address/0xfcba3e75865d2d561be8d220616520c171f12851#code>`_
   sUSD, `StableSwapSUSD.vy <https://github.com/curvefi/curve-contract/blob/master/contracts/pools/susd/StableSwapSUSD.vy>`_, `0xA5407eAE9Ba41422680e2e00537571bcC53efBfD <https://etherscan.io/address/0xA5407eAE9Ba41422680e2e00537571bcC53efBfD#code>`_
   sUSD, `CurveTokenV1.vy <https://github.com/curvefi/curve-contract/blob/master/contracts/tokens/CurveTokenV1.vy>`_, `0xC25a3A3b969415c80451098fa907EC722572917F <https://etherscan.io/address/0xC25a3A3b969415c80451098fa907EC722572917F#code>`_
   USDT, `DepositUSDT.vy <https://github.com/curvefi/curve-contract/blob/master/contracts/pools/usdt/DepositUSDT.vy>`_, `0xac795D2c97e60DF6a99ff1c814727302fD747a80 <https://etherscan.io/address/0xac795d2c97e60df6a99ff1c814727302fd747a80#code>`_
   USDT, `StableSwapUSDT.vy <https://github.com/curvefi/curve-contract/blob/master/contracts/pools/usdt/StableSwapUSDT.vy>`_, `0x52EA46506B9CC5Ef470C5bf89f17Dc28bB35D85C <https://etherscan.io/address/0x52EA46506B9CC5Ef470C5bf89f17Dc28bB35D85C#code>`_
   USDT, `CurveTokenV1.vy <https://github.com/curvefi/curve-contract/blob/master/contracts/tokens/CurveTokenV1.vy>`_, `0x9fC689CCaDa600B6DF723D9E47D84d76664a1F23 <https://etherscan.io/address/0x9fC689CCaDa600B6DF723D9E47D84d76664a1F23#code>`_
   Y, `DepositY.vy <https://github.com/curvefi/curve-contract/blob/master/contracts/pools/y/DepositY.vy>`_, `0xbBC81d23Ea2c3ec7e56D39296F0cbB648873a5d3 <https://etherscan.io/address/0xbbc81d23ea2c3ec7e56d39296f0cbb648873a5d3#code>`_
   Y, `StableSwapY.vy <https://github.com/curvefi/curve-contract/blob/master/contracts/pools/y/StableSwapY.vy>`_, `0x45F783CCE6B7FF23B2ab2D70e416cdb7D6055f51 <https://etherscan.io/address/0x45F783CCE6B7FF23B2ab2D70e416cdb7D6055f51#code>`_
   Y, `CurveTokenV1.vy <https://github.com/curvefi/curve-contract/blob/master/contracts/tokens/CurveTokenV1.vy>`_, `0xdF5e0e81Dff6FAF3A7e52BA697820c5e32D806A8 <https://etherscan.io/address/0xdF5e0e81Dff6FAF3A7e52BA697820c5e32D806A8#code>`_
   Yv2, `StableSwapYv2.vy <https://github.com/curvefi/curve-contract/blob/master/contracts/pools/yv2/StableSwapYv2.vy>`_, `0x8925D9d9B4569D737a48499DeF3f67BaA5a144b9 <https://etherscan.io/address/0x8925D9d9B4569D737a48499DeF3f67BaA5a144b9#code>`_
   Yv2, `CurveTokenV3.vy <https://github.com/curvefi/curve-contract/blob/master/contracts/tokens/CurveTokenV3.vy>`_, `0x571FF5b7b346F706aa48d696a9a4a288e9Bb4091 <https://etherscan.io/address/0x571FF5b7b346F706aa48d696a9a4a288e9Bb4091#code>`_


Meta Pools
----------

Metapools allow for one token to seemingly trade with another underlying base pool. For instance, the GUSD metapool (``[GUSD, [3Pool]]``) contains GUSD and LP tokens of the 3pool (3CRV). This allows for trades between GUSD and any of the three tokens from the 3Pool (DAI, USDC and USDT).

Here is a list of all meta pools currently in use: 

.. csv-table:: 
   :header: "Pool", "Source", "Address"

   bBTC, `StableSwapBBTC.vy <https://github.com/curvefi/curve-contract/blob/master/contracts/pools/bbtc/StableSwapBBTC.vy>`_, `0x071c661B4DeefB59E2a3DdB20Db036821eeE8F4b <https://etherscan.io/address/0x071c661B4DeefB59E2a3DdB20Db036821eeE8F4b#code>`_
   bBTC, `DepositBBTC.vy <https://github.com/curvefi/curve-contract/blob/master/contracts/pools/bbtc/DepositBBTC.vy>`_, `0xC45b2EEe6e09cA176Ca3bB5f7eEe7C47bF93c756 <https://etherscan.io/address/0xC45b2EEe6e09cA176Ca3bB5f7eEe7C47bF93c756#code>`_
   bBTC, `CurveTokenV3.vy <https://github.com/curvefi/curve-contract/blob/master/contracts/tokens/CurveTokenV3.vy>`_, `0x410e3E86ef427e30B9235497143881f717d93c2A <https://etherscan.io/address/0x410e3E86ef427e30B9235497143881f717d93c2A#code>`_
   DUSD, `DepositDUSD.vy <https://github.com/curvefi/curve-contract/blob/master/contracts/pools/dusd/DepositDUSD.vy>`_, `0x61E10659fe3aa93d036d099405224E4Ac24996d0 <https://etherscan.io/address/0x61E10659fe3aa93d036d099405224E4Ac24996d0#code>`_
   DUSD, `StableSwapDUSD.vy <https://github.com/curvefi/curve-contract/blob/master/contracts/pools/dusd/StableSwapDUSD.vy>`_, `0x8038C01A0390a8c547446a0b2c18fc9aEFEcc10c <https://etherscan.io/address/0x8038C01A0390a8c547446a0b2c18fc9aEFEcc10c#code>`_
   DUSD, `CurveTokenV2.vy <https://github.com/curvefi/curve-contract/blob/master/contracts/tokens/CurveTokenV2.vy>`_, `0x3a664Ab939FD8482048609f652f9a0B0677337B9 <https://etherscan.io/address/0x3a664Ab939FD8482048609f652f9a0B0677337B9#code>`_
   GUSD, `StableSwapGUSD.vy <https://github.com/curvefi/curve-contract/blob/master/contracts/pools/gusd/StableSwapGUSD.vy>`_, `0x4f062658EaAF2C1ccf8C8e36D6824CDf41167956 <https://etherscan.io/address/0x4f062658EaAF2C1ccf8C8e36D6824CDf41167956>`_
   GUSD, `DepositGUSD.vy <https://github.com/curvefi/curve-contract/blob/master/contracts/pools/gusd/DepositGUSD.vy>`_, `0x64448B78561690B70E17CBE8029a3e5c1bB7136e <https://etherscan.io/address/0x64448B78561690B70E17CBE8029a3e5c1bB7136e#code>`_
   GUSD, `CurveTokenV2.vy <https://github.com/curvefi/curve-contract/blob/master/contracts/tokens/CurveTokenV2.vy>`_, `0xD2967f45c4f384DEEa880F807Be904762a3DeA07 <https://etherscan.io/address/0xD2967f45c4f384DEEa880F807Be904762a3DeA07#code>`_
   HUSD, `DepositHUSD.vy <https://github.com/curvefi/curve-contract/blob/master/contracts/pools/husd/DepositHUSD.vy>`_, `0x09672362833d8f703D5395ef3252D4Bfa51c15ca <https://etherscan.io/address/0x09672362833d8f703D5395ef3252D4Bfa51c15ca#code>`_
   HUSD, `StableSwapHUSD.vy <https://github.com/curvefi/curve-contract/blob/master/contracts/pools/husd/StableSwapHUSD.vy>`_, `0x3eF6A01A0f81D6046290f3e2A8c5b843e738E604 <https://etherscan.io/address/0x3eF6A01A0f81D6046290f3e2A8c5b843e738E604#code>`_
   HUSD, `CurveTokenV2.vy <https://github.com/curvefi/curve-contract/blob/master/contracts/tokens/CurveTokenV2.vy>`_, `0x5B5CFE992AdAC0C9D48E05854B2d91C73a003858 <https://etherscan.io/address/0x5B5CFE992AdAC0C9D48E05854B2d91C73a003858#code>`_
   LinkUSD, `DepositLinkUSD.vy <https://github.com/curvefi/curve-contract/blob/master/contracts/pools/linkusd/DepositLinkUSD.vy>`_, `0x1de7f0866e2c4adAC7b457c58Cc25c8688CDa1f2 <https://etherscan.io/address/0x1de7f0866e2c4adAC7b457c58Cc25c8688CDa1f2#code>`_
   LinkUSD, `StableSwapLinkUSD.vy <https://github.com/curvefi/curve-contract/blob/master/contracts/pools/linkusd/StableSwapLinkUSD.vy>`_, `0xE7a24EF0C5e95Ffb0f6684b813A78F2a3AD7D171 <https://etherscan.io/address/0xE7a24EF0C5e95Ffb0f6684b813A78F2a3AD7D171#code>`_
   LinkUSD, `CurveTokenV2.vy <https://github.com/curvefi/curve-contract/blob/master/contracts/tokens/CurveTokenV2.vy>`_, `0x6D65b498cb23deAba52db31c93Da9BFFb340FB8F <https://etherscan.io/address/0x6D65b498cb23deAba52db31c93Da9BFFb340FB8F#code>`_
   MUSD, `DepositMUSD.vy <https://github.com/curvefi/curve-contract/blob/master/contracts/pools/musd/DepositMUSD.vy>`_, `0x803A2B40c5a9BB2B86DD630B274Fa2A9202874C2 <https://etherscan.io/address/0x803A2B40c5a9BB2B86DD630B274Fa2A9202874C2#code>`_
   MUSD, `StableSwapMUSD.vy <https://github.com/curvefi/curve-contract/blob/master/contracts/pools/musd/StableSwapMUSD.vy>`_, `0x8474DdbE98F5aA3179B3B3F5942D724aFcdec9f6 <https://etherscan.io/address/0x8474DdbE98F5aA3179B3B3F5942D724aFcdec9f6#code>`_
   MUSD, `CurveTokenV2.vy <https://github.com/curvefi/curve-contract/blob/master/contracts/tokens/CurveTokenV2.vy>`_, `0x1AEf73d49Dedc4b1778d0706583995958Dc862e6 <https://etherscan.io/address/0x1AEf73d49Dedc4b1778d0706583995958Dc862e6#code>`_
   oBTC, `DepositOBTC.vy <https://github.com/curvefi/curve-contract/blob/master/contracts/pools/obtc/DepositOBTC.vy>`_, `0xd5BCf53e2C81e1991570f33Fa881c49EEa570C8D <https://etherscan.io/address/0xd5BCf53e2C81e1991570f33Fa881c49EEa570C8D#code>`_
   oBTC, `StableSwapOBTC.vy <https://github.com/curvefi/curve-contract/blob/master/contracts/pools/obtc/StableSwapOBTC.vy>`_, `0xd81dA8D904b52208541Bade1bD6595D8a251F8dd <https://etherscan.io/address/0xd81dA8D904b52208541Bade1bD6595D8a251F8dd#code>`_
   oBTC, `CurveTokenV3.vy <https://github.com/curvefi/curve-contract/blob/master/contracts/tokens/CurveTokenV3.vy>`_, `0x2fE94ea3d5d4a175184081439753DE15AeF9d614 <https://etherscan.io/address/0x2fE94ea3d5d4a175184081439753DE15AeF9d614#code>`_
   pBTC, `DepositPBTC.vy <https://github.com/curvefi/curve-contract/blob/master/contracts/pools/pbtc/DepositPBTC.vy>`_,`0x11F419AdAbbFF8d595E7d5b223eee3863Bb3902C <https://etherscan.io/address/0x11F419AdAbbFF8d595E7d5b223eee3863Bb3902C#code>`_
   pBTC, `StableSwapPBTC.vy <https://github.com/curvefi/curve-contract/blob/master/contracts/pools/pbtc/StableSwapPBTC.vy>`_, `0x7F55DDe206dbAD629C080068923b36fe9D6bDBeF <https://etherscan.io/address/0x7F55DDe206dbAD629C080068923b36fe9D6bDBeF#code>`_
   pBTC, `CurveTokenV2.vy <https://github.com/curvefi/curve-contract/blob/master/contracts/tokens/CurveTokenV2.vy>`_, `0xDE5331AC4B3630f94853Ff322B66407e0D6331E8 <https://etherscan.io/address/0xDE5331AC4B3630f94853Ff322B66407e0D6331E8#code>`_
   RSV, `DepositRSV.vy <https://github.com/curvefi/curve-contract/blob/master/contracts/pools/rsv/DepositRSV.vy>`_, `0xBE175115BF33E12348ff77CcfEE4726866A0Fbd5 <https://etherscan.io/address/0xBE175115BF33E12348ff77CcfEE4726866A0Fbd5#code>`_
   RSV, `StableSwapRSV.vy <https://github.com/curvefi/curve-contract/blob/master/contracts/pools/rsv/StableSwapRSV.vy>`_, `0xC18cC39da8b11dA8c3541C598eE022258F9744da <https://etherscan.io/address/0xC18cC39da8b11dA8c3541C598eE022258F9744da#code>`_
   RSV, `CurveTokenV2.vy <https://github.com/curvefi/curve-contract/blob/master/contracts/tokens/CurveTokenV2.vy>`_, `0xC2Ee6b0334C261ED60C72f6054450b61B8f18E35 <https://etherscan.io/address/0xC2Ee6b0334C261ED60C72f6054450b61B8f18E35#code>`_
   tBTC, `DepositTBTC.vy <https://github.com/curvefi/curve-contract/blob/master/contracts/pools/tbtc/DepositTBTC.vy>`_, `0xaa82ca713D94bBA7A89CEAB55314F9EfFEdDc78c <https://etherscan.io/address/0xaa82ca713D94bBA7A89CEAB55314F9EfFEdDc78c#code>`_
   tBTC, `StableSwapTBTC.vy <https://github.com/curvefi/curve-contract/blob/master/contracts/pools/tbtc/StableSwapTBTC.vy>`_, `0xC25099792E9349C7DD09759744ea681C7de2cb66 <https://etherscan.io/address/0xC25099792E9349C7DD09759744ea681C7de2cb66#code>`_
   tBTC, `CurveTokenV2.vy <https://github.com/curvefi/curve-contract/blob/master/contracts/tokens/CurveTokenV2.vy>`_, `0x64eda51d3Ad40D56b9dFc5554E06F94e1Dd786Fd <https://etherscan.io/address/0x64eda51d3Ad40D56b9dFc5554E06F94e1Dd786Fd#code>`_
   USDK, `DepositUSDK.vy <https://github.com/curvefi/curve-contract/blob/master/contracts/pools/usdk/DepositUSDK.vy>`_, `0xF1f85a74AD6c64315F85af52d3d46bF715236ADc <https://etherscan.io/address/0xF1f85a74AD6c64315F85af52d3d46bF715236ADc#code>`_
   USDK, `StableSwapUSDK.vy <https://github.com/curvefi/curve-contract/blob/master/contracts/pools/usdk/StableSwapUSDK.vy>`_, `0x3E01dD8a5E1fb3481F0F589056b428Fc308AF0Fb <https://etherscan.io/address/0x3E01dD8a5E1fb3481F0F589056b428Fc308AF0Fb#code>`_
   USDK, `CurveTokenV2.vy <https://github.com/curvefi/curve-contract/blob/master/contracts/tokens/CurveTokenV2.vy>`_, `0x97E2768e8E73511cA874545DC5Ff8067eB19B787 <https://etherscan.io/address/0x97E2768e8E73511cA874545DC5Ff8067eB19B787#code>`_
   USDN, `DepositUSDN.vy <https://github.com/curvefi/curve-contract/blob/master/contracts/pools/usdn/DepositUSDN.vy>`_, `0x094d12e5b541784701FD8d65F11fc0598FBC6332 <https://etherscan.io/address/0x094d12e5b541784701FD8d65F11fc0598FBC6332#code>`_
   USDN, `StableSwapUSDN.vy <https://github.com/curvefi/curve-contract/blob/master/contracts/pools/usdn/StableSwapUSDN.vy>`_, `0x0f9cb53Ebe405d49A0bbdBD291A65Ff571bC83e1 <https://etherscan.io/address/0x0f9cb53Ebe405d49A0bbdBD291A65Ff571bC83e1#code>`_
   USDN, `CurveTokenV2.vy <https://github.com/curvefi/curve-contract/blob/master/contracts/tokens/CurveTokenV2.vy>`_, `0x4f3E8F405CF5aFC05D68142F3783bDfE13811522 <https://etherscan.io/address/0x4f3E8F405CF5aFC05D68142F3783bDfE13811522#code>`_
   UST, `DepositUST.vy <https://github.com/curvefi/curve-contract/blob/master/contracts/pools/ust/DepositUST.vy>`_, `0xB0a0716841F2Fc03fbA72A891B8Bb13584F52F2d <https://etherscan.io/address/0xB0a0716841F2Fc03fbA72A891B8Bb13584F52F2d#code>`_
   UST, `StableSwapUST.vy <https://github.com/curvefi/curve-contract/blob/master/contracts/pools/ust/StableSwapUST.vy>`_, `0x890f4e345B1dAED0367A877a1612f86A1f86985f <https://etherscan.io/address/0x890f4e345B1dAED0367A877a1612f86A1f86985f#code>`_
   UST, `CurveTokenV3.vy <https://github.com/curvefi/curve-contract/blob/master/contracts/tokens/CurveTokenV3.vy>`_, `0x94e131324b6054c0D789b190b2dAC504e4361b53 <https://etherscan.io/address/0x94e131324b6054c0D789b190b2dAC504e4361b53#code>`_


Burners
-------

Burners are a fundamental component of the fee payout mechanism in Curve. A burner converts collected pool fees to an asset which can be converted to USDC. Ultimately, the exchanged for USDC is deposited to the 3Pool, as fees are paid out in 3CRV to veCRV holders. Depending on which tokens a pool contains, a specific burner implementation is used.

Here is a list of all burner contracts currently in use:

.. csv-table::
   :header: "Gauge", "Source", "Address"

   ABurner, `ABurner.vy <https://github.com/curvefi/curve-dao-contracts/blob/master/contracts/burners/ABurner.vy>`_, `0x12220a63a2013133d54558c9d03c35288eac9b34 <https://etherscan.io/address/0x12220a63a2013133d54558c9d03c35288eac9b34#code>`_
   BTCBurner, `BTCBurner.vy <https://github.com/curvefi/curve-dao-contracts/blob/master/contracts/burners/BTCBurner.vy>`_, `0xf9fc73496484290142ee856639f69e04465985cd <https://etherscan.io/address/0xf9fc73496484290142ee856639f69e04465985cd#code>`_
   CBurner, `CBurner.vy <https://github.com/curvefi/curve-dao-contracts/blob/master/contracts/burners/CBurner.vy>`_, `0xdd0e10857d952c73b2fa39ce86308299df8774b8 <https://etherscan.io/address/0xdd0e10857d952c73b2fa39ce86308299df8774b8#code>`_
   ETHBurner, `ETHBurner.vy <https://github.com/curvefi/curve-dao-contracts/blob/master/contracts/burners/ETHBurner.vy>`_, `0xe1ea5d59082bb2165b1bbb93d85492e671fd0969 <https://etherscan.io/address/0xe1ea5d59082bb2165b1bbb93d85492e671fd0969#code>`_
   EuroBurner, `EuroBurner.vy <https://github.com/curvefi/curve-dao-contracts/blob/master/contracts/burners/EuroBurner.vy>`_, `0xcfbd5a821d5fc6bd311abe584e1455d8552b58c0 <https://etherscan.io/address/0xcfbd5a821d5fc6bd311abe584e1455d8552b58c0#code>`_
   LPBurner, `LPBurner.vy <https://github.com/curvefi/curve-dao-contracts/blob/master/contracts/burners/LPBurner.vy>`_, `0xaa42C0CD9645A58dfeB699cCAeFBD30f19B1ff81 <https://etherscan.io/address/0xaa42C0CD9645A58dfeB699cCAeFBD30f19B1ff81#code>`_
   MetaBurner, `MetaBurner.vy <https://github.com/curvefi/curve-dao-contracts/blob/master/contracts/burners/MetaBurner.vy>`_, `0xE4b65889469ad896e866331f0AB5652C1EcfB3E6 <https://etherscan.io/address/0xE4b65889469ad896e866331f0AB5652C1EcfB3E6#code>`_
   USDNBurner, `USDNBurner.vy <https://github.com/curvefi/curve-dao-contracts/blob/master/contracts/burners/USDNBurner.vy>`_, `0x06534b0BF7Ff378F162d4F348390BDA53b15fA35 <https://etherscan.io/address/0x06534b0BF7Ff378F162d4F348390BDA53b15fA35#code>`_
   UnderlyingBurner, `UnderlyingBurner.vy <https://github.com/curvefi/curve-dao-contracts/blob/master/contracts/burners/UnderlyingBurner.vy>`_, `0x786b374b5eef874279f4b7b4de16940e57301a58 <https://etherscan.io/address/0x786b374b5eef874279f4b7b4de16940e57301a58#code>`_
   UniswapBurner, `UniswapBurner.vy <https://github.com/curvefi/curve-dao-contracts/blob/master/contracts/burners/UniswapBurner.vy>`_, `0xf3b64840b39121b40d8685f1576b64c157ce2e24 <https://etherscan.io/address/0xf3b64840b39121b40d8685f1576b64c157ce2e24#code>`_
   YBurner, `YBurner.vy <https://github.com/curvefi/curve-dao-contracts/blob/master/contracts/burners/YBurner.vy>`_, `0xd16ea3e5681234da84419512eb597362135cd8c9 <https://etherscan.io/address/0xd16ea3e5681234da84419512eb597362135cd8c9#code>`_


Liquidity Gauges
----------------

Liquidity Gauges are used to stake LP tokens and handle distribution of the CRV governance token and are part of the Curve DAO.

Here is a list of all liquidity gauges currently in use:

.. csv-table::
   :header: "Gauge", "Source", "Address"
   
   3pool, `LiquidityGauge.sol <https://github.com/curvefi/curve-contract/blob/master/contracts/gauges/LiquidityGauge.vy>`_, `0xbFcF63294aD7105dEa65aA58F8AE5BE2D9d0952A <https://etherscan.io/address/0xbFcF63294aD7105dEa65aA58F8AE5BE2D9d0952A#code>`_
   AAVE, `LiquidityGaugeV2.vy <https://github.com/curvefi/curve-dao-contracts/blob/master/contracts/gauges/LiquidityGaugeV2.vy>`_, `0xd662908ADA2Ea1916B3318327A97eB18aD588b5d <https://etherscan.io/address/0xd662908ADA2Ea1916B3318327A97eB18aD588b5d#code>`_
   ankrETH, `LiquidityGaugeV2.vy <https://github.com/curvefi/curve-dao-contracts/blob/master/contracts/gauges/LiquidityGaugeV2.vy>`_, `0x6d10ed2cF043E6fcf51A0e7b4C2Af3Fa06695707 <https://etherscan.io/address/0x6d10ed2cF043E6fcf51A0e7b4C2Af3Fa06695707#code>`_
   bBTC, `LiquidityGaugeV2.vy <https://github.com/curvefi/curve-dao-contracts/blob/master/contracts/gauges/LiquidityGaugeV2.vy>`_, `0xdFc7AdFa664b08767b735dE28f9E84cd30492aeE <https://etherscan.io/address/0xdFc7AdFa664b08767b735dE28f9E84cd30492aeE#code>`_
   BUSD, `LiquidityGauge.vy <https://github.com/curvefi/curve-contract/blob/master/contracts/gauges/LiquidityGauge.vy>`_, `0x69Fb7c45726cfE2baDeE8317005d3F94bE838840 <https://etherscan.io/address/0x69Fb7c45726cfE2baDeE8317005d3F94bE838840#code>`_
   Compound, `LiquidityGauge.sol <https://github.com/curvefi/curve-contract/blob/master/contracts/gauges/LiquidityGauge.vy>`_, `0x7ca5b0a2910B33e9759DC7dDB0413949071D7575 <https://etherscan.io/address/0x7ca5b0a2910B33e9759DC7dDB0413949071D7575#code>`_
   DUSD, `LiquidityGaugeReward.vy <https://github.com/curvefi/curve-contract/blob/master/contracts/gauges/LiquidityGaugeReward.vy>`_, `0xAEA6c312f4b3E04D752946d329693F7293bC2e6D <https://etherscan.io/address/0xAEA6c312f4b3E04D752946d329693F7293bC2e6D#code>`_
   EURS, `LiquidityGaugeV2.vy <https://github.com/curvefi/curve-dao-contracts/blob/master/contracts/gauges/LiquidityGaugeV2.vy>`_, `0x90Bb609649E0451E5aD952683D64BD2d1f245840 <https://etherscan.io/address/0x90Bb609649E0451E5aD952683D64BD2d1f245840#code>`_
   GUSD, `LiquidityGauge.vy <https://github.com/curvefi/curve-contract/blob/master/contracts/gauges/LiquidityGauge.vy>`_, `0xC5cfaDA84E902aD92DD40194f0883ad49639b023 <https://etherscan.io/address/0xC5cfaDA84E902aD92DD40194f0883ad49639b023#code>`_
   hBTC, `LiquidityGauge.vy <https://github.com/curvefi/curve-contract/blob/master/contracts/gauges/LiquidityGauge.vy>`_, `0x4c18E409Dc8619bFb6a1cB56D114C3f592E0aE79 <https://etherscan.io/address/0x4c18E409Dc8619bFb6a1cB56D114C3f592E0aE79#code>`_
   HUSD, `LiquidityGauge.vy <https://github.com/curvefi/curve-contract/blob/master/contracts/gauges/LiquidityGauge.vy>`_, `0x2db0E83599a91b508Ac268a6197b8B14F5e72840 <https://etherscan.io/address/0x2db0E83599a91b508Ac268a6197b8B14F5e72840#code>`_
   MUSD, `LiquidityGaugeReward.vy <https://github.com/curvefi/curve-contract/blob/master/contracts/gauges/LiquidityGaugeReward.vy>`_, `0x5f626c30EC1215f4EdCc9982265E8b1F411D1352 <https://etherscan.io/address/0x5f626c30EC1215f4EdCc9982265E8b1F411D1352#code>`_
   oBTC, `LiquidityGaugeV2.vy <https://github.com/curvefi/curve-dao-contracts/blob/master/contracts/gauges/LiquidityGaugeV2.vy>`_, `0x11137B10C210b579405c21A07489e28F3c040AB1 <https://etherscan.io/address/0x11137B10C210b579405c21A07489e28F3c040AB1#code>`_
   PAX, `LiquidityGauge.vy <https://github.com/curvefi/curve-contract/blob/master/contracts/gauges/LiquidityGauge.vy>`_, `0x64E3C23bfc40722d3B649844055F1D51c1ac041d <https://etherscan.io/address/0x64E3C23bfc40722d3B649844055F1D51c1ac041d#code>`_
   pBTC, `LiquidityGaugeV2.vy <https://github.com/curvefi/curve-dao-contracts/blob/master/contracts/gauges/LiquidityGaugeV2.vy>`_, `0xd7d147c6Bb90A718c3De8C0568F9B560C79fa416 <https://etherscan.io/address/0xd7d147c6Bb90A718c3De8C0568F9B560C79fa416#code>`_
   renBTC, `LiquidityGauge.vy <https://github.com/curvefi/curve-contract/blob/master/contracts/gauges/LiquidityGauge.vy>`_, `0xB1F2cdeC61db658F091671F5f199635aEF202CAC <https://etherscan.io/address/0xB1F2cdeC61db658F091671F5f199635aEF202CAC#code>`_
   RSV, `LiquidityGaugeReward.vy <https://github.com/curvefi/curve-contract/blob/master/contracts/gauges/LiquidityGaugeReward.vy>`_, `0x4dC4A289a8E33600D8bD4cf5F6313E43a37adec7 <https://etherscan.io/address/0x4dC4A289a8E33600D8bD4cf5F6313E43a37adec7#code>`_
   sAAVE, `LiquidityGaugeV2.vy <https://github.com/curvefi/curve-dao-contracts/blob/master/contracts/gauges/LiquidityGaugeV2.vy>`_, `0x462253b8F74B72304c145DB0e4Eebd326B22ca39 <https://etherscan.io/address/0x462253b8F74B72304c145DB0e4Eebd326B22ca39#code>`_
   sBTC, `LiquidityGaugeReward.vy <https://github.com/curvefi/curve-contract/blob/master/contracts/gauges/LiquidityGaugeReward.vy>`_, `0x705350c4BcD35c9441419DdD5d2f097d7a55410F <https://etherscan.io/address/0x705350c4BcD35c9441419DdD5d2f097d7a55410F#code>`_
   sETH, `LiquidityGaugeV2.vy <https://github.com/curvefi/curve-dao-contracts/blob/master/contracts/gauges/LiquidityGaugeV2.vy>`_, `0x3C0FFFF15EA30C35d7A85B85c0782D6c94e1d238 <https://etherscan.io/address/0x3C0FFFF15EA30C35d7A85B85c0782D6c94e1d238#code>`_
   stETH, `LiquidityGaugeV2.vy <https://github.com/curvefi/curve-dao-contracts/blob/master/contracts/gauges/LiquidityGaugeV2.vy>`_, `0x182B723a58739a9c974cFDB385ceaDb237453c28 <https://etherscan.io/address/0x182B723a58739a9c974cFDB385ceaDb237453c28#code>`_
   sUSDv2, `LiquidityGaugeReward.vy <https://github.com/curvefi/curve-contract/blob/master/contracts/gauges/LiquidityGaugeReward.vy>`_, `0xA90996896660DEcC6E997655E065b23788857849 <https://etherscan.io/address/0xA90996896660DEcC6E997655E065b23788857849#code>`_
   tBTC, `LiquidityGaugeReward.vy <https://github.com/curvefi/curve-contract/blob/master/contracts/gauges/LiquidityGaugeReward.vy>`_, `0x6828bcF74279eE32f2723eC536c22c51Eed383C6 <https://etherscan.io/address/0x6828bcF74279eE32f2723eC536c22c51Eed383C6#code>`_
   USDK, `LiquidityGauge.vy <https://github.com/curvefi/curve-contract/blob/master/contracts/gauges/LiquidityGauge.vy>`_, `0xC2b1DF84112619D190193E48148000e3990Bf627 <https://etherscan.io/address/0xC2b1DF84112619D190193E48148000e3990Bf627#code>`_
   USDN, `LiquidityGauge.vy <https://github.com/curvefi/curve-contract/blob/master/contracts/gauges/LiquidityGauge.vy>`_, `0xF98450B5602fa59CC66e1379DFfB6FDDc724CfC4 <https://etherscan.io/address/0xF98450B5602fa59CC66e1379DFfB6FDDc724CfC4#code>`_
   USDT, `LiquidityGauge.vy <https://github.com/curvefi/curve-contract/blob/master/contracts/gauges/LiquidityGauge.vy>`_, `0xBC89cd85491d81C6AD2954E6d0362Ee29fCa8F53 <https://etherscan.io/address/0xBC89cd85491d81C6AD2954E6d0362Ee29fCa8F53#code>`_
   UST, `LiquidityGaugeV2.vy <https://github.com/curvefi/curve-dao-contracts/blob/master/contracts/gauges/LiquidityGaugeV2.vy>`_, `0x3B7020743Bc2A4ca9EaF9D0722d42E20d6935855 <https://etherscan.io/address/0x3B7020743Bc2A4ca9EaF9D0722d42E20d6935855#code>`_
   Y, `LiquidityGauge.vy <https://github.com/curvefi/curve-contract/blob/master/contracts/gauges/LiquidityGauge.vy>`_, `0xFA712EE4788C042e2B7BB55E6cb8ec569C4530c1 <https://etherscan.io/address/0xFA712EE4788C042e2B7BB55E6cb8ec569C4530c1#code>`_
   Yv2, `LiquidityGaugeV2.vy <https://github.com/curvefi/curve-dao-contracts/blob/master/contracts/gauges/LiquidityGaugeV2.vy>`_, `0x8101E6760130be2C8Ace79643AB73500571b7162 <https://etherscan.io/address/0x8101E6760130be2C8Ace79643AB73500571b7162#code>`_

Pool Registry
-------------

The pool registry serves as an on-chain information hub about the current state of Curve pools. For instance, on-chain integrators can fetch the current address of a Curve pool and query information about it.

Here is a list of all components of the pool registry currently in use:

.. csv-table::
   :header: "Name", "Source", "Address"

   Address Provider, `AddressProvider.vy <https://github.com/curvefi/curve-pool-registry/blob/master/contracts/AddressProvider.vy>`_, `0x0000000022d53366457f9d5e68ec105046fc4383 <https://etherscan.io/address/0x0000000022d53366457f9d5e68ec105046fc4383#code>`_
   Curve Calculator, `CurveCalc.vy <https://github.com/curvefi/curve-pool-registry/blob/master/contracts/CurveCalc.vy>`_, `0xc1DB00a8E5Ef7bfa476395cdbcc98235477cDE4E <https://etherscan.io/address/0xc1DB00a8E5Ef7bfa476395cdbcc98235477cDE4E#code>`_
   Pool Info, `PoolInfo.vy <https://github.com/curvefi/curve-pool-registry/blob/master/contracts/PoolInfo.vy>`_, `0xe64608E223433E8a03a1DaaeFD8Cb638C14B552C <https://etherscan.io/address/0xe64608E223433E8a03a1DaaeFD8Cb638C14B552C#code>`_
   Registry, `Registry.vy <https://github.com/curvefi/curve-pool-registry/blob/master/contracts/Registry.vy>`_, `0x7D86446dDb609eD0F5f8684AcF30380a356b2B4c <https://etherscan.io/address/0x7D86446dDb609eD0F5f8684AcF30380a356b2B4c#code>`_


Curve DAO
---------

Curve DAO consists of multiple smart contracts connected by `Aragon <https://github.com/aragon/aragonOS>`_. Interaction with Aragon occurs through a `modified implementation <https://github.com/curvefi/curve-aragon-voting>`_ of the `Aragon Voting App <https://github.com/aragon/aragon-apps/tree/master/apps/voting>`_. Aragon's standard one token, one vote method is replaced with a weighting system based on locking tokens. Curve DAO has a token (CRV) which is used for both governance and value accrual.

View the `documentation <https://github.com/curvefi/curve-dao-contracts/blob/master/doc/readme.pdf>`_ for an in-depth overview of how the Curve DAO works.

Here is a list of the contracts currently deployed that are used in the Curve DAO:

.. csv-table::
   :header: "Name", "Source", "Address"

   CRV Token, `ERC20CRV.sol <https://github.com/curvefi/curve-dao-contracts/blob/master/contracts/ERC20CRV.vy>`_, `0xD533a949740bb3306d119CC777fa900bA034cd52 <https://etherscan.io/address/0xD533a949740bb3306d119CC777fa900bA034cd52#code>`_
   Fee Distributor, `FeeDistributor.vy <https://github.com/curvefi/curve-dao-contracts/blob/master/contracts/FeeDistributor.vy>`_, `0xA464e6DCda8AC41e03616F95f4BC98a13b8922Dc <https://etherscan.io/address/0xA464e6DCda8AC41e03616F95f4BC98a13b8922Dc#code>`_
   Gauge Controller, `GaugeController.vy <https://github.com/curvefi/curve-dao-contracts/blob/master/contracts/GaugeController.vy>`_, `0x2F50D538606Fa9EDD2B11E2446BEb18C9D5846bB <https://etherscan.io/address/0x2F50D538606Fa9EDD2B11E2446BEb18C9D5846bB#code>`_
   Gauge Proxy, `GaugeProxy.vy <https://github.com/curvefi/curve-dao-contracts/blob/master/contracts/GaugeProxy.vy>`_, `0x519AFB566c05E00cfB9af73496D00217A630e4D5 <https://etherscan.io/address/0x519AFB566c05E00cfB9af73496D00217A630e4D5#code>`_
   Minter, `Minter.vy <https://github.com/curvefi/curve-dao-contracts/blob/master/contracts/Minter.vy>`_, `0xd061D61a4d941c39E5453435B6345Dc261C2fcE0 <https://etherscan.io/address/0xd061D61a4d941c39E5453435B6345Dc261C2fcE0#code>`_
   Pool Proxy, `PoolProxy.vy <https://github.com/curvefi/curve-dao-contracts/blob/master/contracts/PoolProxy.vy>`_, `0x6e8f6D1DA6232d5E40b0B8758A0145D6C5123eB7 <https://etherscan.io/address/0x6e8f6D1DA6232d5E40b0B8758A0145D6C5123eB7#code>`_
   Voting Escrow, `VotingEscrow.vy <https://github.com/curvefi/curve-dao-contracts/blob/master/contracts/VotingEscrow.vy>`_, `0x5f3b5DfEb7B28CDbD7FAba78963EE202a494e2A2 <https://etherscan.io/address/0x5f3b5DfEb7B28CDbD7FAba78963EE202a494e2A2#code>`_
   Vesting Escrow, `VestingEscrow.vy <https://github.com/curvefi/curve-dao-contracts/blob/master/contracts/VestingEscrow.vy>`_, `0x575ccd8e2d300e2377b43478339e364000318e2c <https://etherscan.io/address/0x575ccd8e2d300e2377b43478339e364000318e2c#code>`_
