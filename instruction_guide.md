## Introduction

Welcome to **Bot Father Bundler**—your all-in-one tool for launching tokens with multiple wallets on Pump.Fun. This guide walks you through creating a **20-wallet bundle**. If you get stuck at any point, join our support group on Telegram:

> **Telegram**: [https://t.me/Bot\_Mafia\_Support](https://t.me/Bot_Mafia_Support)
> *– AL THE BOT FATHER*

---

## Prerequisites

* A paid (non-free) RPC endpoint (e.g. Helius, QuickNode).

  > **⚠️ WARNING**: Mainnet or free‐tier RPCs are rate-limited—transactions **will** fail.
* Enough SOL in your accounts to cover fees (Jito, service fee, dev buy, etc.).
* Your token’s metadata (symbol, name, decimals, image file, socials, etc.).

---

## 1. Create a New Bundle

1. Open the **Bundle Mgmt** tab.
2. Click **New Bundle**.
3. Enter a descriptive **Bundle Name**.

---

## 2. Configure RPC

1. In the bundle’s settings, select **Bundle Type**.
2. Paste your paid RPC URL.
3. Click **Save**.

---

## 3. Generate or Import Funder

1. Go to the **Funder** tab.
2. **Option A: Generate a brand-new funder**

   * Click **Generate Funder** → **Generate**.
3. **Option B: Import an existing funder**

   * Click **Import Funder**, paste your base58 private key, and click **OK**.
4. **Fund your Funder**

   * Transfer enough SOL into the funder’s address.
   * Click **Refresh SOL Balance** to confirm receipt.

> **⚠️ NOTE**: Always leave enough SOL in the funder to recover funds at the end.

---

## 4. Generate Dev Wallet and Bundle Wallets

1. Switch to the **Wallets** tab.
2. Click **Generate Dev** → **Generate** to create your dev wallet.
3. Click **Generate Wallet**.

   * Enter **Number of Wallets** (up to 20) → **Generate Wallets**.

---

## 5. Distribute SOL to Bundle Wallets

1. Return to the **Funder** tab.
2. Click **Distribute SOL**.
3. Enter the amount for each wallet (or use **Quick Set**).
4. Optional: enable **Anti-Bubble Map**.
5. Click **Distribute Funds**.
6. When done, go back to **Wallets** → **Refresh Balances**.

> **❗ IMPORTANT**
>
> * The **dev wallet** will pay all fees—include enough SOL to cover Jito tips, service fees, and your dev buy.
> * Don’t drain the funder completely; reserve some SOL for later recovery.

---

## 6. Configure Your Token

1. Open the **Token** tab → **Token Data**.
2. Fill in:

   * Token Name
   * Symbol
   * Description
3. Upload your token image file.
4. (Optional) Social-media links.
5. (Optional) Click **Import Mint** to pull from an existing `mint.json`. Use pf_grinder.exe to grind a keypair with "pump" suffix. 
6. Click **Save**.

---

## 7. Set Buy Parameters

1. Click **Buy Settings**.
2. For both **Dev** and **Bundle Wallets**, set your target buy amounts.
3. (Optional) Adjust **Jito Tip**, **Slippage**, and **Unit Budget**—defaults work in most cases.
4. (Optional) Use **Quick Set Amount** to auto-populate.
5. Click **Save**.

> **❗ REMINDER** The dev wallet must hold enough SOL to cover all fee components and your initial buy.

---

## 8. (If Using >16 Wallets) Create a Lookup Address Table (LUT)

> Use LUT only when you have **17–20** wallets.

1. Click **Lookup Address Table**.
2. Click **Create LUT** → **Yes**.
3. Wait for confirmation (“transaction finalized”), then click **OK**.

---

## 9. Verify Your Bundle

1. Click **Verify**.
2. Resolve any errors listed—verification must pass before launch.

---

## 10. Launch Your Token

1. With everything verified, click **Launch** → **Yes**.
2. Monitor the **Launch Log** for success or errors.
3. (Optional) Click the Pump.Fun link to view your live token.
4. Close the dialog and proceed to the **Sell Console**.

> **Common Failure**: Dev wallet out of funds. Double-check your SOL balance before launching.

---

## 11. Sell Console Workflow

1. Open **Sell Console** tab.
2. Click **Refresh Balances** to update SOL & token balances.
3. Configure your sell parameters.

   * (Optional) Select **Pump.Swap** if your token has bonded.
4. (Optional) Transfer tokens back to the dev wallet:

   * Select wallets (or **Select All**).
   * Click **Tx Tokens to Dev**.
   * Transfer will leave 100 tokens in the bundle wallets so users can close accounts gracefully and recover rent.
   * Click **Refresh Balances** again.
5. When ready, select wallets (or **Select All**) → **Sell Tokens**.
6. Click **Refresh Balances** to confirm.

---

## 12. Recover Remaining SOL

1. Go to the **Funder** tab → **Recover SOL**.
2. Click **Select All** → **Recover SOL** (pulls SOL from dev + bundle wallets back into funder).
3. Switch to **Wallets** → **Refresh Balances** to verify.

---

## 13. Transfer Out & Drain Funder (Optional)

* To send SOL elsewhere: enter a receiver’s public key and amount, then **Send** (leave a little SOL for fees).
* To drain the funder fully: click **Drain Funder Wallet**, enter the recipient’s PubKey & PrivKey, and **Send**.

---

## 14. Remove Your Bundle

1. Return to **Bundle Mgmt**.
2. Select your bundle from **Available Bundles** → **Remove Bundle** → **Yes**.

---

## 15. Key Management Tips

* In any table (Funder, Wallets, Sell Console), **right-click** a row to:

  * Copy PubKey
  * Copy Private Key
  * Open on Solscan

> 🔒 All bundle data is saved as a JSON file in your `bundles` directory for later reference.

---

You’re all set! Follow these steps in order, watch for warnings, and your 20-wallet token launch should go smoothly. If anything trips you up, hop into our Telegram and let us know. Good luck!
