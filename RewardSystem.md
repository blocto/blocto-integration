# Send Reward API

## Domains
| Environment        | Domain           |
| ------------- |:-------------:|
| Staging      | api-staging.blocto.app |
| Production      | api.blocto.app |

## Header
`Authorization`: `<JWT>`

`Content-Type`: `application/json`

## APIs

### /reward/send [POST]
Send reward by blockchain and blocto wallet address.

#### Request:
```
{
  'blockchain': 'ethereum',
  'wallet_address': '0x8A6a17F1A3DA0F407A67BF8E076Ed7F678D85f29',
  'point': 100,
}
```

#### Response:
```
{
  'message_code': ok
}
```
