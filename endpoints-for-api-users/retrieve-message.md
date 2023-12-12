# Retrieve Message

Retrieves a single message and its delivery status.

We currently do not support pushing webhooks to your server when the status of a message changes.

{% code title="Endpoint #2" overflow="wrap" %}
```sh
GET /campaigns/:campaignId/messages/:messageId
```
{% endcode %}

{% code title="Example response body" overflow="wrap" %}
```json
{
  "id": "message_62a2a141-97f8-4fc8-82db-36f539228322",
  "recipient": "+6599999999",
  "language": "english",
  "values": {
    "recipientName": "Emily Yeo",
    "topic": "passport application #12345F"
  },
  "latestStatus": "success",
  "error": ""
}
```
{% endcode %}

