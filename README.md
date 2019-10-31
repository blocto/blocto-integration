# Portto-Notification-APIs
| Environment        | Domain           |
| ------------- |:-------------:|
| Staging      | api-staging.blocto.app |
| Production      | api.blocto.app |

## Header
`Authorization`: `<JWT>`

`Content-Type`: `application/json`

## APIs

### /notification/send [POST]
Send notification by user_ids or tag.(tag is higher priority than user_ids)

If tag is present in request, user_ids will be ignored.

#### Request:
```
{
  'user_ids': [
    '<user id>',
    ...
  ],
  'tags': [
    '<users match the tag>',
    ...
  ],
  'text': 'any text showing on content',
  'url': 'the url direct to'
}
```

#### Response:
```
{
  'message_code': ok
}
```

### /notification/tag [POST]
Tag users by user_id

#### Request:
```
{
  'user_ids': [
    '<user id>',
    ...
  ],
  'tag': '<user tag>'
}
```

#### Response:
```
{
  'message_code': ok
}
```

## Web App
Blocto injects a global API into websites at `window.bloctoProvider` and `window.{network}` at the same time. Currently, Blocto suppports networks:

- `ethereum`
- `tangerine`

### Register Push Notification
```
let web3 = new Web3(window.ethereum) // or window.tangerine or window.bloctoProvider
if (web3.currentProvider.isBlocto) {
  let encryptedUserId = await web3.currentProvider.registerPushNotification("{appId}")
  // send encryptedUserId to your backend
}
```