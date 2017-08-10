# codeless 

## Introduction

Codeless, no coding work to integrate analytics on your Facebook chatbot, or Facebook page!  And there are some advantages to use codeless integration:

* No need to change your chatbot code, no side effects.
* Messenger platform handles message tracking, so the server load on your own server is reduced.

## How it works

Now, only Facebook Messenger enables codeless integration, while other message platforms don't, this is because: 

* You can bind more than one webhook to a single Facebook page.
* Webhook collects both incoming and outgoing (echo) messages.

## How to use it

- step 0. Create Botimize project and obtain the API Key
- setp 1. Login [Facebook Developer](https://developers.facebook.com/) 
- step 2. Create or choose an existing Facebook App, if it's your first time creating Facebook App, [take this reference](https://developers.facebook.com/docs/apps/register)

- step 3. Add Product: Messenger

![codeless_step3](imgs/codeless_step3.png "90%x")

- step 4. Obtain the page access token of the page
![codeless_step4-1](imgs/codeless_step4-1.png "90%x")
![codeless_step4-2](imgs/codeless_step4-2.png "90%x")

- step 5. Go to project setting page of Botimize and create a webhook, enter the access token from step 4. This will give you a webhook URL.
![codeless_step5-1](imgs/codeless_step5-1.png "90%x")
![codeless_step5-2](imgs/codeless_step5-2.png "90%x")
![codeless_step5-3](imgs/codeless_step5-3.png "90%x")

- step 6. Go to Facebook App main page, Add Product: Webhooks
![codeless_step6-1](imgs/codeless_step6-1.png "90%x")

- step 6. Go to Webhook setting page, Add subscribe, choose your page and enter the URL from step 5.
![codeless_step7-1](imgs/codeless_step7-1.png "90%x")
![codeless_step7-2](imgs/codeless_step7-2.png "90%x")
