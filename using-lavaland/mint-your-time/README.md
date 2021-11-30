# Mint your TIME (🫖, 🫖)

The Mint page allow users to mint TIME from the protocol at a discount by trading it with i) **liquidity** (LP tokens) or ii) **other assets**. The former is called liquidity minting and the latter reserve minting.

The minting action create bonds which take roughly 15 epochs to vest, and TIME tokens are vested linearly to the user over that period. Liquidity minting help the protocol to accumulate and lock liquidity, while reserve minting allow the protocol to grow its treasury, and thus its Backing per TIME faster.

**​**[**Wonderland**](https://app.wonderland.money/bonds) offers currently different types of assets that can be used to mint TIME on its website:

_The "Legacy Website" Button in the bottom left part of the screen will redirect you to the previous UI of Wonderland!_

### &#x20;<a href="#settings" id="settings"></a>

Settings is a feature that allows you to mint **TIME** while sending the acquired **TIME** to another address. This is useful for additional privacy, or for minting multiple TIME while the current mints are still vesting. Note that if the same account holds multiple mints, the pending rewards from the earlier mints have to be forfeited. _Note: What this means in practice, is that if a user has vested rewards from a previous minting action purchase, and he then mints another TIME, the 5 days timer is resetted for all the rewards, and the vesting period will start again._

1.  1\.

    Go to [**Mint**](https://app.wonderland.money/#/mints) page and select the assets you want to use to mint TIMEs.
2.  2\.

    Select the amount that you would like to mint, then click on the cogwheel icon at the top right of the page.
3.  3\.

    The **Settings** menu will show up. At the Recipient Address field, you can specify a different address that will receive the vested **TIME**. By default, it is filled with your current address.
4.  4\.

    You can also modify the **Slippage** field to increase or decrease the likelihood of your order getting through. A higher slippage increases that likelihood, but you may get a more undesirable fill price.
5.  5\.

    Close the **Settings** menu by clicking the cross icon.
6.  6\.

    Click "Approve" and sign the transaction.
7.  7\.

    After the "Approve" transaction has been processed successfully, click "Mint" and sign the transaction. Voila, you have minted your firdst **TIME** tokens using the Settings!

![](<../../.gitbook/assets/Screenshot 2021 10 25 at 15.35.19>)

* _The "Approve" transaction is only needed when minting for the first time; subsequent minting only requires you to perform the "mint" transaction._
* _When using Settings, do not alter the mint amount after you have closed the Settings menu, as it will reset the recipient address._

### &#x20;<a href="#how-to-redeem" id="how-to-redeem"></a>

Go to the [**Mint**](https://app.wonderland.money/#/mints) page and select the bond type you have purchased. Select the "Redeem" tab.

Use the **Claim** to claim all of your available rewards**,** and have the pending TIME sent to your wallet.

Use the **Claim and Autostake** button to have all the available TIME sent automatically to the staking contract and receive the MEMOries as a receipt for your stake!

![](<../../.gitbook/assets/Screenshot 2021 10 25 at 15.37.16>)

### &#x20;<a href="#reading-the-info" id="reading-the-info"></a>

#### &#x20;<a href="#bond-page" id="bond-page"></a>

* **MINT Price** is the price of **TIME** you get from minting. You can calculate the mint price using the following formulae: - LP Mint: (Value of your LP token / TIME you'll get from minting) - MIM Mint: (Value of your MIM token / TIME you'll get from minting)
* **TIME Price** is the market price of **TIME**.
* **Your Balance** is your balance of LP tokens or asset used to mint.
* **You Will Get** tells you how many **TIME** tokens you will get from minting.
* **Max You can Buy** maximum amount of TIME available to be bought.
* **Debt Ratio** measures the total amount of TIME created from mints that have yet to be paid out by the protocol. The debt ratio is calculated differently for LP mints and MIM mints: - LP Mint: (**TIME** created from unredeemed mints / **TIME** total supply) - MIM Mint: (**TIME** created from unredeemed mints / **TIME** circulating supply)
* **Vesting Term** measures the period a minting action takes to fully redeem. This number is expressed in days.
* **Minimum Purchase**: Minimum amount of **TIME** that can be minted

#### &#x20;<a href="#redeem-page." id="redeem-page."></a>

* **Time Until fully vested** time until the TIME minted will be fully redeemable
* **Pending Rewards** is the amount of **TIME** you are entitled to receive from minting.
* **Claimable Rewards** is the amount of **TIME** that you can claim now. This amount keeps increasing as **TIME** is vested to you over the vesting period.
* **ROI** is the Return On Investment
* **Vesting Term** measures the period a Minting action takes to fully redeem. This number is expressed in days.

![](<../../.gitbook/assets/Screenshot 2021 10 25 at 15.41.09>)
