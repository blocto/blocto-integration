# Blocto Integration

Blocto is the easiest dapp browser ever created. With Blocto you can get access blockchain technology easily. We use meta-transaction to pay gas fee for users, so users can start trying your dapp even they don't have any cryptocurrency.

### Download
- App Store: <https://apps.apple.com/app/blocto/id1481181682>
- Google Pay: <https://play.google.com/store/apps/details?id=com.portto.blocto>

## Web3 Provider
Blocto injects a global API into websites at `window.bloctoProvider` and `window.{network}` at the same time. Currently, Blocto suppports networks:

- `ethereum`
- `tangerine`

If user is on Ethereum network, the provider will be injected at `window.bloctoProvider` and `window.ethereum`.

### Sign Message
The api to call signing message is not different with other private key based wallets. The only difference is that the return value contains multiple signatures because Blocto is a smart contract based wallet. Therefore, please follow [EIP-1654](https://github.com/ethereum/EIPs/issues/1654) to verify the signature. There are some open-source implementations of EIP-1654 signature verification: [go](https://github.com/dapperlabs/dappauth) [js](https://github.com/dapperlabs/dappauth.js).

### Send Transaction
You don't need to change anything. If it works with MetaMask, it will also work on Blocto.

### Send Batch Transaction
Please take a look at [web3 doc](https://web3js.readthedocs.io/en/v1.2.0/web3-eth.html#batchrequest). For general web3 provider, BatchRequest send all transactions simultaneously. For Blocto provider, it will combine multiple transactions (in order) into **ONE** transaction. If one of transactions fails, all transactions will fail. This method can also save a lot of gas.

If you would like to know more technical details, please see the smart contract code: [Etherscan](https://etherscan.io/address/0xed69ac1cab88cc82ff417131bdc69d93427107b4#code)


## Deep Linking

### Open Blocto dapp browser with a url and blockchain network
- `url`: dapp website url
- `blockchain`: optional parameter. Currently, Blocto suppports networks:

<https://blocto.app/link?url=https://knightstory.io&blockchain=ethereum>

We will automatically detect that user is on Android/iOS/Web and show different CTA button on the webpage.

## Push Notification
Read more on <a href="PushNotification.md">PushNotification</a>.

## Contact Us
If you have any questions, please feel free to contact us: <dev@portto.io>