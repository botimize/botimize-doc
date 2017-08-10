## Initialization
  ```javascript
  const botimize = require('botimize')('<YOUR-BOTIMIZE-API-KEY>', 'facebook');
  ```

## Log Incoming Messages
  ```javascript
  app.post('/webhook', function (req, res)) {
    botimize.logIncoming(req.body); // <--- add this line where your receive incoming request
  }
  ```

## Log Outgoing Messages
- For those who already use request to your poject: Put options of request into `logOutgoing()`.
  ```javascript
  let options = {
    uri: 'https://graph.facebook.com/v2.6/me/messages',
    qs: { access_token: accessToken },
    method: 'POST',
    json: true,
    body: messageBody,
  };
  request(options, function (error, response, body) {
    botimize.logOutgoing(options, {parse: 'request'});
    ...
  });
  ```

- For those who are not using request to send outgoing messages: Use data format structure listed as below.
  ```javascript
  let data = {
    ...messageBody,
    accessToken,
  };
  botimize.logOutgoing(data, {parse: 'pure'});
  ```
  ```javascript
  let data = {
    recipient: { id: '1487766407960998' },
    message: 'hello facebook messenger',
    accessToken: 'EAAXUgsVmiP8BAMcRWxLa1N5RycMzZBfjwiekoqCik6pZASPsnmkJtG29gp5QXdyMaKfFg0iZCIDlqhfhTZCLqRKuM4hUCfdZBcxl8GzKgZA0AwI8syxG49M9OaZCsjyZC8FPg30yIRDFG5hp9jNNtvqtWW0KKzB9a59rTkZBsgz2oe4QZDZD'
  };
  botimize.logOutgoing(data, {parse: 'pure'});
  ```
  