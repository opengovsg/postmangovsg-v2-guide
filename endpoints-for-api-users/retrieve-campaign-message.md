# Retrieve Campaign Message

Retrieves messages and their delivery statuses given a campaign ID, as well as information about the campaign template. Please refer to this table in [Possible message statuses and what they mean](../faq/postman-v2-sms-api-faq/message-statuses.md) on what each message status means.

{% code title="Endpoint #5" %}
```
GET /campaigns/:campaignId/messages
```
{% endcode %}

### **Supported Query Parameters**

#### **`limit`** string (Mandatory)&#x20;

You can specify the number of messages to return per page using the limit query parameter. The minimum value is 1, and the maximum value is 1000.

#### **`after`** string (Optional)&#x20;

Find messages after the cursorId

#### **`before`** string (Optional)&#x20;

Find messages before the cursorId

#### **`search`** string (Optional)&#x20;

This supports searching by recipient phone number only. It is a substring match, eg. a "11" would match with "91122233"

{% code title="Response Body" %}
```json
{
	"data": [
		{
			"createdAt": "2024-02-27T16:12:52.710+08:00",
			"updatedAt": "2024-02-27T16:13:03.027+08:00",
			"id": "message_44b63f2b-1cd0-5b9d-a8e2-5ca716fe2745",
			"recipient": "6599999999",
			"values": {
				"name": "test2"
			},
			"fullMessage": "Open Government Products\n\n---\n\nDear test2, hello!\n\n---\n\n\This is an automated SMS from the Singapore Government. Please do not reply.",
			"latestStatus": "success",
			"templateBodyId": "<YOUR_TEMPLATE_BODY_ID>",
			"campaignId": "<YOUR_CAMPAIGN_ID>",
			"templateBody": {
				"createdAt": "2024-02-27T16:10:20.299+08:00",
				"updatedAt": "2024-02-27T16:10:20.299+08:00",
				"id": "<YOUR_TEMPLATE_BODY_ID>",
				"templateId": "<YOUR_TEMPLATE_ID>",
				"language": "english",
				"body": "Dear {{name}}, hello!",
				"creatorId": "<YOUR_CREATOR_ID>"
			},
			"batches": [
				{
					"createdAt": "2024-02-27T16:11:47.007+08:00",
					"updatedAt": "2024-02-27T16:12:52.824+08:00",
					"id": "<YOUR_BATCH_ID>",
					"originalFileName": "(sample) Test.csv",
					"status": "success",
					"campaignId": "<YOUR_CAMPAIGN_ID>",
					"creatorId": "<YOUR_CREATOR_ID>",
					"totalMessages": 1,
					"BatchMessage": {
						"createdAt": "2024-02-27T16:12:52.714+08:00",
						"updatedAt": "2024-02-27T16:12:52.714+08:00",
						"id": "<BATCH_MESSAGE_ID>",
						"batchId": "<YOUR_BATCH_ID>",
						"messageId": "<YOUR_MESSAGE_ID>"
					}
				}
			],
			"language": "english",
			"batchId": "<YOUR_BATCH_ID>"
		}
	],
	"pageData": {
		"hasNextPage": false,
		"hasPreviousPage": false,
		"startCursor": "WyIyMDI0LTAyLTI3VDE2OjEyOjUyLjcxMCswODowMCIsIm1lc3NhZ2VfNDRiNjNmMmItMWNkMC01YjlkLWE4ZTItNWNhNzE2ZmUyNzQ1Il0=",
		"endCursor": "WyIyMDI0LTAyLTI3VDE2OjEwOjUxLjg0OSswODowMCIsIm1lc3NhZ2VfYzkyM2FmYzktMTgwNi00MDc4LTlmNDAtMmMyM2U3NzU3YzFmIl0="
	}
}
```
{% endcode %}
