# Equations

### &#x20;<a href="#staking" id="staking"></a>

deposit=withdrawaldeposit = withdrawal

Swaps between **TIME** and **MEMOries** during staking and unstaking are always honored 1:1. The amount of TIME deposited into the staking contract will always result in the same amount of **MEMOries**. And the amount of MEMOries withdrawn from the staking contract will always result in the same amount of TIME.

rebase=1−(TIMEDeposits/MEMOriesOutstanding)rebase = 1 - ( TIMEDeposits / MEMOries Outstanding )

The treasury deposits TIME into the distributor. The distributor then deposits TIME into the staking contract, creating an imbalance between TIME and MEMOries. MEMOries is rebased to correct this imbalance between TIME deposited and MEMOries outstanding. The rebase brings MEMOries outstanding back up to parity so that 1 MEMOries equals 1 staked TIME.

### &#x20;<a href="#minting" id="minting"></a>

Minting happens by allowing users to purchase a bond. This bond price is the Mint price.

bondPrice=1+Premiumbond Price = 1 + Premium

TIME has an intrinsic value of 1 MIM, which is roughly equivalent to $1. In order to make a profit from minting, **Wonderland** charges a premium for each minting action.

Premium=debtRatio∗BCVPremium = debt Ratio \* BCV

The premium is derived from the debt ratio of the system and a scaling variable called BCV. BCV allows us to control the rate at which bond prices increase.

The premium determines profit due to the protocol and in turn, stakers. This is because new TIME is minted from the profit and subsequently distributed among all stakers.

debtRatio=bondsOutstanding/TIMESupplydebt Ratio = bondsOutstanding/TIMESupply

The debt ratio is the total of all TIME promised to bonders divided by the total supply of TIME. This allows us to measure the debt of the system.

bondPayoutreserveBond=marketValueasset / bondPricebondPayout\_{reserveBond} = marketValue\_{asset}\ /\ bondPrice

Bond payout determines the number of TIME sold to a minter. For reserve mints, the market value of the assets supplied by the minter is used to determine the bond payout. For example, if a user supplies 1000 MIM and the mint price is 250 MIM, the user will be entitled 4 TIME.

bondPayoutlpBond=marketValuelpToken / bondPricebondPayout\_{lpBond} = marketValue\_{lpToken}\ /\ bondPrice

For liquidity mints, the market value of the LP tokens supplied by the minter is used to determine the bond payout. For example, if a user supplies 0.001 TIME-AVAX LP token which is valued at 1000 MIM at the time of bonding, and the bond price is 250 MIM, the user will be entitled 4 TIME.

### &#x20;<a href="#time-supply" id="time-supply"></a>

TIMEsupplyGrowth=TIMEstakers+TIMEbonders+TIMEDAOTIME\_{supplyGrowth} = TIME\_{stakers} + TIME\_{bonders} + TIME\_ {DAO}

TIME supply does not have a hard cap. Its supply increases when:

* TIME is minted and distributed to the stakers.
* TIME is minted for the bonder. This happens whenever someone purchases a bond.
* TIME is minted for the DAO. This happens whenever someone purchases a bond. The DAO gets the same number of TIME as the bonder.

TIMEstakers=TIMEtotalSupply∗rewardRateTIME\_{stakers} = TIME\_{totalSupply} \* rewardRate

At the end of each epoch, the treasury mints TIME at a set reward rate. These TIME will be distributed to all the stakers in the protocol.

TIMEbonders=bondPayoutTIME\_{bonders} = bondPayout

Whenever someone purchases a bond, a set number of TIME is minted. These TIME will not be released to the minter all at once - they are vested to the bonder linearly over time. The bond payout uses a different formula for different types of bonds. Check the Minting section above to see how it is calculated.

TIMEDAO=TIMEbondersTIME\_{DAO} = TIME\_{bonders}

The DAO receives the same amount of TIME as the minter. This represents the DAO profit.

### &#x20;<a href="#backing-per-time" id="backing-per-time"></a>

TIMEbacking=treasuryBalancestablecoin+treasuryBalanceotherAssetsTIME\_{backing} = treasuryBalance\_{stablecoin} + treasuryBalance\_{otherAssets}

Every TIME in circulation is backed by the **Wonderland** treasury. The assets in the treasury can be divided into two categories: stablecoin and non-stablecoin.

treasuryBalancestablecoin=BackingPerTIMEreserveBond+BackingPerTIMElpBondtreasuryBalance\_{stablecoin} = BackingPerTIME\_{reserveBond} + BackingPerTIME\_{lpBond}

The stablecoin balance in the treasury grows when bonds are sold. Backing per TIME is calculated differently for different mints types.

BackingPerTIMEreserveBond=assetSuppliedBackingPerTIME\_{reserveBond} = assetSupplied

For reserve mints such as MIM minting, the Backing per TIME simply equals to the amount of the underlying asset supplied by the minter.

BackingPerTIMElpBond=2sqrt(constantProduct)∗(% ownership of the pool)BackingPerTIME\_{lpBond} = 2sqrt(constantProduct) \* (\\%\ ownership\ of\ the\ pool)

For LP Mints such as TIME-AVAX Minting, the RBacking Per TIME is calculated differently because the protocol needs to mark down its value. _Why?_ The LP token pair consists of TIME, and each TIME in circulation will be backed by these LP tokens - there is a cyclical dependency. To safely guarantee all circulating TIME are backed, the protocol marks down the value of these LP tokens.
