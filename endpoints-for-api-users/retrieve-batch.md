# Retrieve Batch

Retrieves messages and their delivery statuses given a batch ID. Please refer to this table in [possible message statuses](the-message-object.md#lateststatus-string) and what they mean on what each message status means.

{% code title="Endpoint #4" %}
```sh
GET /campaigns/:campaignId/batch/:batchId/messages
```
{% endcode %}

### Supported Query Parameters

#### `limit` string (Mandatory)

You can specify the number of messages to return per page using the `limit` query parameter. The minimum value is 1, and the maximum value is 1000.

#### `after` string (Optional)

Find messages after the cursorId

#### `before` string (Optional)

Find messages before the cursorId

#### `search` string (Optional)

This supports searching by recipient phone number only.

It is a substring match, eg. a "11" would match with "91122233"

{% code title="Example response body" overflow="wrap" %}
```json
{
    "data": [
        {
            "createdAt": "2024-01-29T17:47:51.392+08:00",
            "updatedAt": "2024-01-29T17:48:02.562+08:00",
            "id": "<YOUR_MESSAGE_ID>",
            "recipient": "6599999999",
            "values": {
                "name": "john doe",
                "fruit": "apple"
            },
            "fullMessage": "<YOUR_GENERATED_MESSAGE>",
            "latestStatus": "success",
            "templateBodyId": "YOUR_GENERATED_TEMPLATE_ID>",
            "campaignId": "<YOUR_CAMPAIGN_ID>",
            "templateBody": {
                "createdAt": "2023-12-27T16:28:29.242+08:00",
                "updatedAt": "2023-12-27T16:28:29.242+08:00",
                "id": "<",
                "templateId": "<YOUR_GENERATED_TEMPLATE_ID>",
                "language": "english",
                "body": "Dear {{name}}, your favourite food is {{fruit}}",
                "creatorId": "<YOUR_GENERATED_CREATOR_ID>"
            },
            "language": "english"
        }
    ],
    "pageData": {
        "hasNextPage": false,
        "hasPreviousPage": false,
        "startCursor": "WyIyMDI0LTAxLTI5VDE3OjQ3OjUxLjQwMyswODowMCIsIjY4NSJd",
        "endCursor": "WyIyMDI0LTAxLTI5VDE3OjQ3OjUxLjQwMyswODowMCIsIjY4NSJd"
    }
}
```
{% endcode %}
