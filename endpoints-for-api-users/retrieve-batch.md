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
      "id": "message_62a2a141-97f8-4fc8-82db-36f539228322",
      "recipient": "6599999999",
      "values": {
        "recipientName": "Emily Yeo",
        "topic": "passport application #12345F"
      },
      "language": "english",
      "latestStatus": "success",
      "error": ""
    },
    ...
  ],
  "pageData": {
		"hasNextPage": false,
		"hasPreviousPage": false,
		"startCursor": "WyIyMDIzLTEwLTI0VDE3OjQwOjI1Ljk2OCswODowMCIsIm1lc3NhZ2VfM2E1MWI1ODctMzQ5OS00YTBmLTlkNGUtZTRlOWYzNWZkNmMxIl0=",
		"endCursor": "WyIyMDIzLTEwLTI0VDE3OjQwOjI1Ljk2OCswODowMCIsIm1lc3NhZ2VfM2E1MWI1ODctMzQ5OS00YTBmLTlkNGUtZTRlOWYzNWZkNmMxIl0="
	}
}
```
{% endcode %}
