---
{
  "title": "Testnet",
  "description": "A guide on how to use Wasabi on testnet. This is the Wasabi documentation, an archive of knowledge about the open-source, non-custodial and privacy-focused Bitcoin wallet for desktop."
}
---

# Testnet

[[toc]]

---

## Bitcoin testnet

The Bitcoin testnet is a network that behaves almost exactly the same as the Bitcoin mainnet.
The major difference is that the bitcoin on the testnet do not have any economical value, they should not be used to buy or sell goods and services.
This makes the network very useful for testing software and features, because there is no risk of loosing precious "real" bitcoin from the main network.

:::tip Don't loose your bitcoin
When testing cutting edge software like Wasabi, use testnet to ensure that your mistakes don't cost you money!
:::

## Activating testnet in Wasabi

First, open your Wasabi Wallet and go to the `Settings` tab.
Here you find a drop-down menu of which network Wasabi should use, `Main`, `TestNet` or `RegTest`, select `TestNet`.

![](/SettingsNetwork.png)

Notice that the setting does only apply for the next start of Wasabi, so you must close Wasabi, and then re-open it before you are on testnet.
When Wasabi is started in testnet, it will fetch testnet [BIP 158 block filters](/using-wasabi/BIPs.md#bip-158-compact-block-filters-for-light-clients) from the coordinator.
For the first start, this may take a couple of minutes.

After the testing, set the settings back to mainnet, and close Wasabi.
It will load on mainnet the next time you start it.

## Loading a wallet

You can [load](/using-wasabi/WalletLoad.md) any previously generated wallet on testnet, by double clicking on it in the Wallet Explorer.
However, it is recommended to use a dedicated testnet wallet.
Notice that Wasabi uses the same wallet file and keys for both mainnet and testnet, you can load the same wallet file in either network.

## Receiving testnet bitcoin

You can [generate a receive address](/using-wasabi/Receive.md) the same way as on mainnet, by labeling an observer in the `Receive` tab.
Notice that testnet SegWit addresses start with `tb1q...`, and not with `bc1q...` as mainnet addresses.

Because testnet bitcoin don't have economical value, they are gifted by different sources.
There are [faucets](https://en.bitcoin.it/wiki/Testnet#Faucets) like [this one](https://testnet-faucet.mempool.co/) that give a certain amount of testnet bitcoin per time period.
You may also ask other developers if they have a couple spare testnet coins available.

## CoinJoin on testnet

[CoinJoin](/using-wasabi/CoinJoin.md) on testnet is as easy as on mainnet.
In the `CoinJoin` tab, select the coins you want to CoinJoin, enter the password and click `enqueue selected coins`.
Notice that the minimum denomination and anonymity set are much lower on testnet, for example `0.001 btc` and `2 anonymity set`.
This is done to enable many rounds of CoinJoin quickly, the privacy gain does not have to be substantial or efficient, as this is for testing.
Usually there are other testers doing a CoinJoin, but if you are the only one at the moment, then load two wallets and enqueue coins in both of them.
