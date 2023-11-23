# Retrieve Batch

Retrieves messages and their delivery statuses given a batch ID. Please refer to this table in [possible message statuses](the-message-object.md#lateststatus-string) and what they mean on what each message status means.

{% code title="Endpoint" overflow="wrap" %}
```sh
GET /campaigns/:campaignId/bulk/messages/:batchId
```
{% endcode %}

{% code title="Example response body" overflow="wrap" %}
```json
{
  "data": [
    {
      "id": "message_62a2a141-97f8-4fc8-82db-36f539228322",
      "recipient": "+6599999999",
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
