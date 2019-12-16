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