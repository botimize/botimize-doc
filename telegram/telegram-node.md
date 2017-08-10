## Initialization
  ```javascript
  const botimize = require('botimize')('<YOUR-BOTIMIZE-API-KEY>', 'telegram');
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
    uri: `https://api.telegram.org/bot${token}/sendMessage`,
    method: 'POST',
    json: true,
    body: messageBody,
  };
  request(options, function (error, response, body) {
  botimize.logOutgoing(options, {parse: 'request'});
  // ...
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
    chat_id: '161696362',
    text: 'hello telegram',
    token: '308726257:AAHnmJpvkAepqirk82ZOrgtF6Hz2ijbRavA',
  };
  botimize.logOutgoing(data, {parse: 'pure'});
  ```
  