# The message object

```json
//Example response
{
  "id": "message_62a2a141-97f8-4fc8-82db-36f539228322",
  "recipient": "6599999999",
  "language": "english",
  "values": {
    "recipientName": "Emily Yeo",
    "topic": "passport application #12345F"
  },
  "latestStatus": "created",
  "error": ""
}
```

### Attributes

***

**id** string

Message identifier - this can be used to retrieve a single message and its delivery status ([Retrieve message](retrieve-message.md)).

***

**recipient** string (Mandatory field)

For messages sent through the `sms` channel, the recipient will be the mobile phone number of the recipient, prefixed by the country code but without the leading `+`. For example, when sending to a Singaporean phone number, the value of recipient will be `6599999999`

eg. `6591234567` is a recipient string for a Singapore (65) phone number (91234567)

***

**language** string (Mandatory field)

This is the language of the message template used to send this message. One of `english`, `chinese`, `malay`, or `tamil`.

***

**values** object (Mandatory field)

The values that were inserted into the message template and form the complete message. The keys within `values` will vary depending on the campaign’s template parameters.

In the example above, the message template that was used contained two parameters: `recipientName` and `topic`.

Avoid using `recipient` and `language` as keywords as they are mandatory fields in the request payload.

***

#### **latestStatus** string

Possible message statuses and what they mean

| Status    | What it means                                                                                                                                                                                           |
| --------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `created` | <p>Postman is aware of your request and has created the necessary records.</p><p>However, it has not yet made the request to the relevant messaging service provider to have the message sent.</p>      |
| `sent`    | <p>Postman has made the request to the relevant messaging service provider to have the message sent.</p><p>However, it has not yet received a notification from the provider on the request status.</p> |
| `success` | The relevant messaging service provider has sent an update to Postman saying that the message has been delivered to the recipient.                                                                      |
| `failure` | Message failed to send either due to an error in Postman or from the messaging service. More details in the error message.                                                                              |

***

**error** string

The error message if `latestStatus` is `failure`. Conversely, if the `latestStatus` is not `failure`, the value for `error` will be an empty string.
