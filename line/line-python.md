## Initialization
  ```python
  from botimize import Botimize
  botimize = Botimize('<YOUR-API-KEY>', 'line')
  ```

## Log Incoming Messages
  ```python
  botimize.log_incoming(request.body)
  ```

## Log Outgoing Messages
  ```python
  outgoing_log = {
    'replyToken': '9bd439c6961346d7b2ec4184469b9946',
    'messages': [{
      'type': 'text',
      'text': 'hello, this is a message from LINE chatbot',
    }],
    'channelAccessToken': 'GxvuC0QfatJ0/Bv5d3DoVbUcfVd6MXLj9QY8aFHSqCOdkfjD1I5dtbKZBNMbmLmwKox1Ktd0Kcwfsxm9S5OmIwQoChcV1gPlK/1CI8cUe3eqaG/UrqL65y1Birb6rnssT0Acaz+7Lr7V2WVnwrQdB04t89/1O/w1cDnyilFU=',
  }
  botimize.log_outgoing(outgoing_log)
  ```
