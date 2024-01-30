# Retrieve Message

Retrieves a single message and its delivery status.

We currently do not support pushing delivery status to your server via webhooks when the status of a message changes.

{% code title="Endpoint #2" overflow="wrap" %}
```sh
GET /campaigns/:campaignId/messages/:messageId
```
{% endcode %}

{% code title="Example response body" overflow="wrap" %}
```json
{
    "createdAt": "2024-01-29T17:56:49.821+08:00",
    "updatedAt": "2024-01-29T17:57:02.029+08:00",
    "id": "message_d9d8aa47-f369-4aee-b0ae-794e608fa13f",
    "recipient": "659999999",
    "values": {
        "name": "John Doe",
        "fruit": "apple"
    },
    "fullMessage": "<YOUR_FULL_MESSAGE>",
    "latestStatus": "success",
    "templateBodyId": "<YOUR_GENERATED_TEMPLATE_BODY_ID>",
    "templateBody": {
        "createdAt": "2023-12-27T16:28:29.242+08:00",
        "updatedAt": "2023-12-27T16:28:29.242+08:00",
        "id": "<YOUR_GENERATED_ID>",
        "templateId": "<YOUR_GENERATED_TEMPLATE_ID>",
        "language": "english",
        "body": "Dear {{name}}, your favourite food is {{fruit}}",
        "creatorId": "<YOUR_GENERATED_CREATOR_ID>"
    },
    "batches": [],
    "language": "english"
}
```
{% endcode %}
