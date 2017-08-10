## Initialization
  ```javascript
  const botimize = require('botimize')('<YOUR-BOTIMIZE-API-KEY>', 'line');
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
    uri: 'https://api.line.me/v2/bot/message/reply',
    headers: {
      'Authorization': `Bearer ${channelAccessToken}`,
    },
    method: 'POST',
    json: true,
    body: messageBody
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
    channelAccessToken,
  };
  botimize.logOutgoing(data, {parse: 'pure'});
  ```
  ```javascript
  let data = {
    replyToken: '9bd439c6961346d7b2ec4184469b9946',
    messages: [{
      type: 'text',
      text: 'hello, this is a message from LINE chatbot',
    }],
    channelAccessToken: 'GxvuC0QfatJ0/Bv5d3DoVbUcfVd6MXLj9QY8aFHSqCYJkZhKG6u5I5dtbKZBNMbmLmwKox1Ktd0Kcwfsxm9S5OmIwQoChcV1gPlK/1CI8cUe3eqaG/UrqL65y1Birb6rnssT0Acaz+7Lr7V2WVnwrQdB04t89/1O/w1cDnyilFU=',
  };
  botimize.logOutgoing(data, {parse: 'pure'});
  ```
  