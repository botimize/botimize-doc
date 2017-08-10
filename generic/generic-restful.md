## Log incoming messages

Make a `POST` request to `https://api.getbotimize.com/messages?apikey=<API_KEY>`.

Example:

```shell
curl -X POST -H 'Content-Type: application/json' -d '{
  "platform": "generic",
  "direction": "incoming",
  "raw": {
    "timestamp": "<TIME OF MESSAGE(in milliseconds)>",
    "recipient": {
      "id": "<UUID_OF_RECIPIENT>",
      "name": "<NAME_OF_RECIPIENT>"
    },
    "sender": {
      "id": "<UUID_OF_SENDER>",
      "name": "<NAME_OF_SENDER>"
    },
    "message": {
      "type": "<MESSAGE_TYPE>",
      "text": "<MESSAGE_CONTENT>"
    }
  }
}' https://api.getbotimize.com/messages?apikey=<API_KEY>
```

## Log outgoing messages

Make a `POST` request to `https://api.getbotimize.com/messages?apikey=<API_KEY>`.

Example:

```shell
curl -X POST -H 'Content-Type: application/json' -d '{
  "platform": "generic",
  "direction": "outgoing",
  "raw": {
    "timestamp": "<TIME OF MESSAGE(in milliseconds)>",
    "recipient": {
      "id": "<UUID_OF_RECIPIENT>",
      "name": "<NAME_OF_RECIPIENT>"
    },
    "sender": {
      "id": "<UUID_OF_SENDER>",
      "name": "<NAME_OF_SENDER>"
    },
    "message": {
      "type": "<MESSAGE_TYPE>",
      "text": "<MESSAGE_CONTENT>"
    }
  }
}' https://api.getbotimize.com/messages?apikey=<API_KEY>
```
