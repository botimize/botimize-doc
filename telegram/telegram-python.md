## Initialization
  ```python
  from botimize import Botimize
  botimize = Botimize('<YOUR-API-KEY>', 'telegram')
  ```

## Log Incoming Messages
  ```python
  botimize.log_incoming(request.body)
  ```

## Log Outgoing Messages
  ```python
  outgoing_log = {
    'chat_id': '161696362',
    'text': 'hello telegram',
    'token': '308726257:AAHnmJpvkAepqirk82ZOrgtF6Hz2ijbRavA',
  }
  botimize.log_outgoing(outgoing_log)
  ```
