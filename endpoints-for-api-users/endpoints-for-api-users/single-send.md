# Single Send

The keys within the values object will vary depending on the campaign’s template parameters. To find out what the parameters for a template are, please refer to the template’s details in Postman’s web interface.



{% code title="Endpoint #1" overflow="wrap" %}
```
POST /campaigns/:campaignId/messages
```
{% endcode %}

{% code title="Example request body" overflow="wrap" %}
```json
{
  "recipient": "+6599999999",
  "language": "english",
  "values": {
    // The following values are values for the parameters in the example template
    "recipientName": "Emily Yeo",
    "topic": "passport application #12345F"
  },
}
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
  "latestStatus": "created"
}
```
{% endcode %}
