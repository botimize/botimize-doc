## Log incoming messages

Make a `POST` request to `https://api.getbotimize.com/messages?apikey=<API_KEY>`.

Example:

```shell
curl -X POST -H 'Content-Type: application/json' -d '{
  "platform": "line",
  "direction": "incoming",
  "raw": {
    "events":[
        {
            "type":"message",
            "replyToken":"6a37af4d99a94ce9bbe9184171398b70",
            "source":{
            "userId":"Uc76d8ae9ccd1ada4f06c4e1515d46466",
            "type":"user"
            },
            "timestamp":1492439626890,
            "message":{
            "type":"text",
            "id":"5952264121603",
            "text":"hello"
            }
        }
    ]
  }
}' https://api.getbotimize.com/messages?apikey=<API_KEY>
```

`raw` is the data you webhook received from Line Messenger platform. Check [webhook reference](https://devdocs.line.me/en/#webhook-event-object) for more detail.

## Log outgoing messages

Make a `POST` request to `https://api.getbotimize.com/messages?apikey=<API_KEY>`.

Example:

```shell
curl -X POST -H 'Content-Type: application/json' -d '{
  "platform": "line",
  "direction": "outgoing",
  "raw": {
    "replyToken":"nHuyWiB7yP5Zw52FIkcQobQuGDXCTA",
    "messages":[
      {
        "type":"text",
        "text":"Hello, user"
      },
      {
        "type":"text",
        "text":"May I help you?"
      }
    ]
  }
}' https://api.getbotimize.com/messages?apikey=<API_KEY>
```

`raw` is the data your webhook server sends to Line  platform. Check [send API reference](https://devdocs.line.me/en/?shell#reply-message) for more detail.
