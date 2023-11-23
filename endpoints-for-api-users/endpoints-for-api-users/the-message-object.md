# The message object

### Attributes

***

**id** string

Message identifier - this can be used to retrieve a single message and its delivery status ([Retrieve message](retrieve-message.md)).

***

**recipient** string

For messages sent through the `sms` channel, the recipient will be the mobile phone number of the recipient, prefixed by `+` and country code.

***

**language** string

This is the language of the message template used to send this message. One of `english`, `chinese`, `malay`, or `tamil`.

***

**values** object

The values that were inserted into the message template and form the complete message. The keys within `values` will vary depending on the campaign’s template parameters.

In the example on the right-hand side, the message template that was used contained two parameters: `recipientName` and `topic`.

***

#### **latestStatus** string

Possible message statuses and what they mean

| Status    | What it means                                                                                                                                                                                                  |
| --------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `created` | <p>Postman is aware of your request and has created the necessary records.</p><p></p><p>However, it has not yet made the request to the relevant messaging service provider to have the message sent.</p>      |
| `sent`    | <p>Postman has made the request to the relevant messaging service provider to have the message sent.</p><p></p><p>However, it has not yet received a notification from the provider on the request status.</p> |
| `success` | The relevant messaging service provider has sent an update to Postman saying that the message has been delivered to the recipient.                                                                             |
| `failure` | Message failed to send either due to an error in Postman or from the messaging service. More details in the error message.                                                                                     |

***

**error** string

The error message if `latestStatus` is `failure`. Conversely, if the `latestStatus` is not `failure`, the value for `error` will be an empty string.
