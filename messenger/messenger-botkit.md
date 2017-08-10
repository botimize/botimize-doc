## Facebook Messenger Integration with Botkit and NPM

This middleware plugin for [Botkit](http://howdy.ai/botkit) allows you to seamlessly integrate [botimize](http://getbotimize.com) functionalities into your Botkit bot.

### Setup

- [Create a free account](https://dashboard.getbotimize.com/register) to get an API key.

- Since botimize SDK is a peer dependency, it needs to be installed manually:

  ```shell
  npm install --save botimize
  ```

- Then install this middleware plugin:

  ```shell
  npm install --save botimize-botkit-middleware
  ```

### Usage

* Use API key to create a new botimize and middleware objects:

  ```javascript
  const botimize = require('botimize')('<YOUR-API-KEY'>, 'facebook');
  const botimizeBotkit = require('botimize-botkit-middleware')(botimize);
  ```

* Setup Botkit middleware:

  ```javascript
  const controller = botkit.facebookbot({...});
  controller.middleware.receive.use(botimizeBotkit.receive);
  controller.middleware.send.use(botimizeBotkit.send);
  ```

* Send notifications via email:

  ```javascript
  botimize.notify('<recipient-email>', '<text-content-to-be-sent>');
  ```
