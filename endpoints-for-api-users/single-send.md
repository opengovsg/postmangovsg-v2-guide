# Single Send

The keys within the values object will vary depending on the campaign’s template parameters. To find out what the parameters for a template are, please refer to the template’s details in Postman’s web interface.

The response on whether the message was created will come in immediately. However, you will need to query `Retrieve message endpoint` to get the message `latestStatus`.

{% code title="Endpoint #1" overflow="wrap" %}
```
POST /campaigns/:campaignId/messages
```
{% endcode %}

{% code title="Example request body" overflow="wrap" %}
```json
{
  "recipient": "6599999999",
    "language": "english",
    "values": {
        // The following values are values for the parameters in the example template
        "name": "John Doe",
        "fruit": "apple"}
}
```
{% endcode %}

{% code title="Example response body" overflow="wrap" %}
```json
{
    "createdAt": "2024-01-29T17:39:35.574+08:00",
    "updatedAt": "2024-01-29T17:39:35.574+08:00",
    "id": "<YOUR_GENERATED_MESSAGE_ID>",
    "recipient": "6599999999",
    "values": {
        "name": "John Doe",
        "fruit": "apple"
    },
    "fullMessage": "<YOUR_FULL_MESSAGE>",
    "latestStatus": "created",
    "templateBodyId": "<YOUR_TEMPALTE_BODY_ID>",
    "campaignId": "<YOUR_CAMPAIGN_ID>",
    "language": "english"
}
```
{% endcode %}
