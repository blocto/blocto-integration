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
