## Initialization
Use API key to create a new botimize object

  ```javascript
  const botimize = require('botimize')('<YOUR-API-KEY>', 'generic');
  ```

## Log incoming messages:
 
  ```javascript
  app.post('/webhook', function (req, res)) {
    const incomingLog = {
      sender: {
        id: 'UNIQUE_USER_ID',
        name: 'USER_SCREEN_NAME'
      },
      content: {
        type: 'CONTENT_TYPE', // 'text', 'image', 'audio', 'video', 'file', 'location'
        text: 'CONTENT_TEXT'
      }
    };
    botimize.logIncoming(incomingLog);
    ...
  }
  ```

## Log outgoing messages

  ```javascript
    const outgoingLog = {
      receiver: {
        id: 'UNIQUE_USER_ID',
        name: 'USER_SCREEN_NAME'
      },
      content: {
        type: 'CONTENT_TYPE', // 'text', 'image', 'audio', 'video', 'file', 'location'
        text: 'CONTENT_TEXT'
      }
    };
  request(options, function (error, response, body) {
    botimize.logOutgoing(outgoingLog);
    ...
  });
  ```
