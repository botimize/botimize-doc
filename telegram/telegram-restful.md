## Log incoming messages

Make a `POST` request to `https://api.getbotimize.com/messages?apikey=<API_KEY>`.

Example:

```shell
curl -X POST -H 'Content-Type: application/json' -d '{
  "platform": "telegram",
  "direction": "incoming",
  "raw": {
    "update_id": 39073337,
    "message": {
      "message_id": 69,
      "from": {
        "id": 261354561,
        "first_name": "Bill",
        "last_name": "Gates",
        "username": "bill",
        "language_code": "zh-Hant-TW"
      },
      "chat": {
        "id": 261354561,
        "first_name": "Bill",
        "last_name": "Gates",
        "username": "bill",
        "type": "private"
      },
      "date": 1496917931,
      "text": "hi"
    }
  }
}' https://api.getbotimize.com/messages?apikey=<API_KEY>
```

`raw` is the data you webhook received from Telegram platform. It could be message or post back. Check [webhook reference](https://core.telegram.org/bots/api#getting-updates) for more detail.

## Log outgoing messages

Make a `POST` request to `https://api.getbotimize.com/messages?apikey=<API_KEY>`.

Example:

```shell
curl -X POST -H 'Content-Type: application/json' -d '{
  "platform": "telegram",
  "direction": "outgoing",
  "raw": {
    "chat_id": "161696362",
    "text": "hello telegram",
    "token": "308726257:AAHnmJpvkAepqirk82ZOrgtF6Hz2ijbRavA",
  }
}' https://api.getbotimize.com/messages?apikey=<API_KEY>
```

`raw` is the data your webhook server sends to Telegram platform **including** your page acess token. Check [send API reference](https://core.telegram.org/bots/api#sendmessage) for more detail.
