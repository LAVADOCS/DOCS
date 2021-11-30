# Policy

**​**[**Wonderland**](https://www.wonderland.money/stake) features policy constants that allow us to optimize the system.

### &#x20;<a href="#bonds" id="bonds"></a>

Every time a user Mints TIME on Wonderland, he is actually purchasing a bond. This Bonds have different parameters. The **BCV** allows us to scale the rate at which bond premiums increase. A higher BCV means a lower discount for bonders and more protocol profit. A lower BCV means a higher discount for bonders and less protocol profit.

The **vesting term** determines how long it takes for bonds to become fully redeemable. A longer term means lower inflation and lower bond demand.

### &#x20;<a href="#sales" id="sales"></a>

The **DCV** allows us to scale protocol buy pressure up or down. A higher DCV means more buy pressure and higher deflation. A lower DCV means less buy pressure and a weaker floor.

### &#x20;<a href="#treasury" id="treasury"></a>

Profit Allocations are the only treasury variable. This allows us to choose who receives profits from the protocol.

### &#x20;<a href="#staking" id="staking"></a>

There are no variables in the staking contract. **TIME** and **MEMOries** are always redeemable 1:1, and profits are always distributed equally through rebase.
