# Botkit Starter Kit

This is a Botkit starter kit for slack, created with the [Yeoman generator](https://github.com/howdyai/botkit/tree/master/packages/generator-botkit#readme).

To complete the configuration of this bot, make sure to update the included `.env` file with your platform tokens and credentials.

[Botkit Docs](https://botkit.ai/docs/v4)

This bot is powered by [a folder full of modules](https://botkit.ai/docs/v4/core.html#organize-your-bot-code). 
Edit the samples, and add your own in the [features/](features/) folder.
# blogbuddy

# Steps to Recreate

[Install botkit](https://www.npmjs.com/package/botkit)

[Install and follow setup for ngrok](https://ngrok.com/download) - will be used to expose port 3000

Create new slack app via [Slack API](https://api.slack.com/). This will give you credentials to fill out the .env file in the project folder.
Follow this [article](https://medium.com/better-programming/how-to-build-a-slack-bot-in-2020-592ac92066d8) on how to setup the Slack API. 

Essentially:
1. copy over signing secret to .env
2. OAuth & Permissions -> give bot token scope to the bot (ie chat:write)
3. copy over token to .env 
4. copy ngrok url to Event Subscription (ie mine was https://bb78cbe1e5ab.ngrok.io/api/messages)
5. it won't you save changes for Event Subscription so you have to Subscribe to Bot Events first https://botkit.ai/docs/v4/provisioning/slack-events-api.html
  - message.channels
  - message.groups
  - message.im
  - message.mpim
6. now you should be able to head to Incoming Webhooks and manually send a message to the selected channel


