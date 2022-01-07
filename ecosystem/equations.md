# Equations

### &#x20;<a href="#staking" id="staking"></a>



Swaps between **LAVA** and n**Lava** during staking and unstaking are always honored 1:1. The amount of LAVA deposited into the staking contract will always result in the same amount of n**Lava**. And the amount of sLava withdrawn from the staking contract will always result in the same amount of LAVA.

rebase=1−(LAVADeposits/sLavaOutstanding)rebase = 1 - ( LAVADeposits / sLava Outstanding )

The treasury deposits LAVA into the distributor. The distributor then deposits LAVA into the staking contract, creating an imbalance between LAVA and sLava. sLava is rebased to correct this imbalance between LAVA deposited and sLava outstanding. The rebase brings sLava outstanding back up to parity so that 1 sLava equals 1 staked LAVA.

### &#x20;<a href="#minting" id="minting"></a>

Minting happens by allowing users to purchase a bond. This bond price is the Mint price.

bondPrice=1+Premiumbond Price = 1 + Premium

LAVA has an intrinsic value of 1 DAI, which is roughly equivalent to $1. In order to make a profit from minting, **Lavaland** charges a premium for each minting action.

Premium=debtRatio∗BCVPremium = debt Ratio \* BCV

The premium is derived from the debt ratio of the system and a scaling variable called BCV. BCV allows us to control the rate at which bond prices increase.

The premium determines profit due to the protocol and in turn, stakers. This is because new LAVA is minted from the profit and subsequently distributed among all stakers.

debtRatio=bondsOutstanding/LAVASupplydebt Ratio = bondsOutstanding/LAVASupply

The debt ratio is the total of all LAVA promised to bonders divided by the total supply of LAVA. This allows us to measure the debt of the system.

bondPayoutreserveBond=marketValueasset / bondPricebondPayout\_{reserveBond} = marketValue\_{asset}\ /\ bondPrice

Bond payout determines the number of LAVA sold to a minter. For reserve mints, the market value of the assets supplied by the minter is used to determine the bond payout. For example, if a user supplies 1000 DAI and the mint price is 250 DAI, the user will be entitled 4 LAVA.

bondPayoutlpBond=marketValuelpToken / bondPricebondPayout\_{lpBond} = marketValue\_{lpToken}\ /\ bondPrice

For liquidity mints, the market value of the LP tokens supplied by the minter is used to determine the bond payout. For example, if a user supplies 0.001 LAVA-FTM LP token which is valued at 1000 DAI at the time of bonding, and the bond price is 250 DAI, the user will be entitled 4 LAVA.

### &#x20;<a href="#time-supply" id="time-supply"></a>

LAVAsupplyGrowth=LAVAstakers+LAVAbonders+LAVADAOLAVA\_{supplyGrowth} = LAVA\_{stakers} + LAVA\_{bonders} + LAVA\_ {DAO}

LAVA supply does not have a hard cap. Its supply increases when:

* LAVA is minted and distributed to the stakers.
* LAVA is minted for the bonder. This happens whenever someone purchases a bond.
* LAVA is minted for the DAO. This happens whenever someone purchases a bond. The DAO gets the same number of LAVA as the bonder.

LAVAstakers=LAVAtotalSupply∗rewardRateLAVA\_{stakers} = LAVA\_{totalSupply} \* rewardRate

At the end of each epoch, the treasury mints LAVA at a set reward rate. These LAVA will be distributed to all the stakers in the protocol.

LAVAbonders=bondPayoutLAVA\_{bonders} = bondPayout

Whenever someone purchases a bond, a set number of LAVA is minted. These LAVA will not be released to the minter all at once - they are vested to the bonder linearly over time. The bond payout uses a different formula for different types of bonds. Check the Minting section above to see how it is calculated.

LAVADAO=LAVAbondersLAVA\_{DAO} = LAVA\_{bonders}

The DAO receives the same amount of LAVA as the minter. This represents the DAO profit.

### &#x20;<a href="#backing-per-time" id="backing-per-time"></a>

LAVAbacking=treasuryBalancestablecoin+treasuryBalanceotherAssetsLAVA\_{backing} = treasuryBalance\_{stablecoin} + treasuryBalance\_{otherAssets}

Every LAVA in circulation is backed by the **Lavaland** treasury. The assets in the treasury can be divided into two categories: stablecoin and non-stablecoin.

treasuryBalancestablecoin=BackingPerLAVAreserveBond+BackingPerLAVAlpBondtreasuryBalance\_{stablecoin} = BackingPerLAVA\_{reserveBond} + BackingPerLAVA\_{lpBond}

The stablecoin balance in the treasury grows when bonds are sold. Backing per LAVA is calculated differently for different mints types.

BackingPerLAVAreserveBond=assetSuppliedBackingPerLAVA\_{reserveBond} = assetSupplied

For reserve mints such as DAI minting, the Backing per LAVA simply equals to the amount of the underlying asset supplied by the minter.

BackingPerLAVAlpBond=2sqrt(constantProduct)∗(% ownership of the pool)BackingPerLAVA\_{lpBond} = 2sqrt(constantProduct) \* (\\%\ ownership\ of\ the\ pool)

For LP Mints such as LAVA-FTM Minting, the RBacking Per LAVA is calculated differently because the protocol needs to mark down its value. _Why?_ The LP token pair consists of LAVA, and each LAVA in circulation will be backed by these LP tokens - there is a cyclical dependency. To safely guarantee all circulating LAVA are backed, the protocol marks down the value of these LP tokens.
