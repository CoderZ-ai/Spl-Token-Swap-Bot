Spl token Volume and Trend Bot

First install the required library in Library.

Then add the priva_key of the wallet to be traded in .env.

If you are going to add multiple private keys.

You will add it as privatekey, privakey, privatekey. The last time you add it, it will not be.

Then open main.js file with notepad.

Since my token is OTR, it can write OTR. You don't need to change OTR.

Set this as the mint address of your own token.

const OTR_MINT = new PublicKey(“Your Token”);

The code trades according to the current price, update this part according to your token.

const otrResp = await fetch(“https://api.dexscreener.com/latest/dex/tokens/your mint address of the token”);

If your token is not available. You can use another api provider.

Fee rate is standard : 1000. you can update it here. If the fee rate is low, it will not confirm the transaction.

computeUnitPriceMicroLamports: 2000 //Fee Rate

This part is between left buy and sell. The program sets a random buy or sell amount from 0.3 to 0.6.

swapAmount = randomAmount(0.3, 0.6);

Save and run it.

Start : node main.js
