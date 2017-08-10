## Initialization
  ```python
  from botimize import Botimize
  botimize = Botimize('<YOUR-API-KEY>', 'facebook')
  ```

## Log Incoming Messages
  ```python
  botimize.log_incoming(request.body)
  ```

## Log Outgoing Messages
  ```python
  outgoing_log = {
    'recipient': { 'id': '1487766407960998' },
    'message': 'hello facebook messenger',
    'accessToken': 'EAAXUgsVmiP8BAMcRWxLa1N5RycMzZBfjwiekoqCik6pZASPsnmkJtG29gp5QXdyMaKfFg0iZCIDlqhfhTZCLqRKuM4hUCfdZBcxl8GzKgZA0AwI8syxG49M9OaZCsjyZC8FPg30yIRDFG5hp9jNNtvqtWW0KKzB9a59rTkZBsgz2oe4QZDZD'
  }
  botimize.log_outgoing(outgoing_log)
  ```
