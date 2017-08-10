## Log incoming messages

Make a `POST` request to `https://api.getbotimize.com/messages?apikey=<API_KEY>`.

Example:

```shell
curl -X POST -H 'Content-Type: application/json' -d '{
  "platform": "facebook",
  "direction": "incoming",
  "raw": {
    {
      "object":"page",
      "entry":[
        {
          "id":"PAGE_ID",
          "time":1458692752478,
          "messaging":[
            {
              "sender":{
                "id":"USER_ID"
              },
              "recipient":{
                "id":"PAGE_ID"
              },
            }
          ]
        }
      ]
    }
  }
}' https://api.getbotimize.com/messages?apikey=<API_KEY>
```

`raw` is the data you webhook received from Facebook Messenger platform. It could be message or post back. Check [webhook reference](https://developers.facebook.com/docs/messenger-platform/webhook-reference) for more detail.

## Log outgoing messages

Make a `POST` request to `https://api.getbotimize.com/messages?apikey=<API_KEY>`.

Example:

```shell
curl -X POST -H 'Content-Type: application/json' -d '{
  "platform": "facebook",
  "direction": "outgoing",
  "raw": {
    "access_token": "PAGE_ACCESS_TOKEN",
    "message": {
      "text": "hellow, world!"
    },
    "recipient": {
      "id": "USER_ID"
    }
  }
}' https://api.getbotimize.com/messages?apikey=<API_KEY>
```

`raw` is the data your webhook server sends to Facebook Messenger platform **including** your page acess token. Check [send API reference](https://developers.facebook.com/docs/messenger-platform/send-api-reference/text-message) for more detail.
