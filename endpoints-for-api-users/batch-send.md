# Batch Send

Sends multiple messages in a single API request.

You will need to prepare a CSV file where, in addition to recipient and language, each column represents a value to the campaign’s template parameter.

{% code title="Example CSV File" overflow="wrap" %}
```
recipient,language,recipientName,topic
6599999999,english,Emily Yeo,passport application #12345F
6599999998,chinese,James Tan,passport application #67890A
```
{% endcode %}

You will then need to upload this file to this endpoint.

To upload your file, send a `multipart/form-data` request to this endpoint.

{% code title="Endpoint #3" %}
```sh
POST /campaigns/:campaignId/batch/messages
```
{% endcode %}

If your client code is written in JavaScript, consider using a `FormData` object to contain your file ([MDN Web API docs](https://developer.mozilla.org/en-US/docs/Web/API/FormData/Using\_FormData\_Objects)).

{% code title="Example JavaScript code" overflow="wrap" %}
```javascript
// Assuming you have a constant or variable named "file" which is a File object:

const formData = new FormData();
formData.append("file", file);

const request = new XMLHttpRequest();
request.setRequestHeader("Authorization", "Bearer " + YOUR_API_KEY);
request.open(
  "POST",
  "https://<POSTMAN_V2_API_BASE_URL>/api/v2/campaigns/<YOUR_CAMPAIGN_ID>/batch/messages"
);

request.send(formData);
```
{% endcode %}

{% code title="Response Body" %}
```json
{
  "batchId": "batch_d11eabe6-8454-4934-96a6-4cdb9242412c"
}
```
{% endcode %}
