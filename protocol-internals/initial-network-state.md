# Initial Network State

**Our initial goal is not to find a stable price.** This may seem antithetical to our currency aspirations, but we ensure you it is not. [**Wonderland**](https://www.wonderland.money/stake) can be tuned to optimize for different things. The main tradeoff is volatility and profitability versus stability and consistency. With volatility and profit comes growth; this is what we want early on.

With tight policy and scale, [**Wonderland**](https://www.wonderland.money/stake) should function well as a stable asset. Upward and downward pressures should stabilize at some non-intrinsic value. With loose policy, regardless of scale, Wonderland has the potential to act as a wealth creation machine. The market premium of the token measures the positive sum of the game; all extrinsic value is new wealth created.

### &#x20;<a href="#alpha-state" id="alpha-state"></a>

The initial network features a one-way treasury (money goes in, none comes out), the bonding contract (through which supply increases and profits are produced i.e minting), and the staking contract (where profits are distributed).

The following are the initial policy states:

* **BCV -** BCV varies based on mint types . It is tuned regularly by the Policy team to meet the protocol goals. For example, if the protocol wants to accumulate more liquidity into its treasury, it can lower the BCV for allowing users to mint TIME with LP to increase their bond capacity.
* **Mint vesting term -** It is set to a fixed number Avalanche blocks or approximately five days for all Minting Asset types.
* **TIME distribution -** Every time someone Mints TIME, the proceed will go to the Wonderland Treasury. A corresponding amount of TIME will be minted and distributed to three parties:
  * _Minter -_ The Minter will receive the quoted amount of TIME minted linearly over the vesting term.
  * _DAO -_ The DAO receives the same amount of TIME as the minter. This represents the DAO profit.
  * _Stakers -_ After accounting for the TIME distributed to the minter and the DAO, the rest will be distributed among all stakers in the protocol.
