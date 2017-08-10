## Initialization
Use API key to create a new botimize object

  ```python
  from botimize import Botimize
  botimize = botimize.Botimize('<YOUR-API-KEY>', 'generic')
  ```

## Log incoming messages:
 
  ```python
  incoming_log = {
    'sender': {
      'id': 'UNIQUE_USER_ID',
      'name': 'USER_SCREEN_NAME'
    },
    'content': {
      'type': 'CONTENT_TYPE', #'text', 'image', 'audio', 'video', 'file', 'location'
      'text': 'CONTENT_TEXT'
    }
  }
  botimize.log_incoming(incoming_log)
  ```

## Log outgoing messages

  ```python
  outgoing_log = {
    'receiver': {
      'id': 'UNIQUE_USER_ID',
      'name': 'USER_SCREEN_NAME'
    },
    'content': {
      'type': 'CONTENT_TYPE', #'text', 'image', 'audio', 'video', 'file', 'location'
      'text': 'CONTENT_TEXT'
    }
  }
  botimize.log_outgoing(outgoing_log)
  ```