# 📞 Endpoints for API users

### Message

A message represents a message sent through a campaign.

As each campaign is associated with one message template and has its own API key, you will need to keep track of your API keys if you wish to send messages in different campaigns.

You will not be able to send or retrieve a message in a campaign inaccessible to yourself, even if you know the relevant ID(s).

{% code title="Message-related endpoints" overflow="wrap" %}
```sh

POST /campaigns/:campaignId/messages
GET  /campaigns/:campaignId/messages/:messageId

POST /campaigns/:campaignId/batch/messages
GET  /campaigns/:campaignId/batch/messages/:batchId
```
{% endcode %}
