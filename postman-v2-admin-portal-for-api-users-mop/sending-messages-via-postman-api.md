---
description: How do I send out messages if I want to call Postman's API Endpoints
---

# 🖥️ Sending Messages via Postman API

{% hint style="info" %}
Please ensure that you have read the [Campaign Settings page](campaign-settings.md) before reading this page.&#x20;
{% endhint %}

Before calling Postman's API endpoints, please ensure

1. You are connected to the [whitelisted IP address for this campaign](campaign-settings.md#integrations-ip-address-whitelisting).
2. You have entered the [correct API key](campaign-settings.md#api-keys).

### Multiple message parameters (variables)

In this example, we will be using the following message content with multiple message parameters (variables).

```markup
Dear {{name}}, your next appointment at {{clinic}} is on {{date}} at {{time}} hrs. 
```

#### Request Body example

{% code title="Example Request Body" %}
```json
{
    "recipient": "6599999999",
    "language": "english",
    "values": {
        // The following values are values for the parameters in the example template
        "name": "John Doe",
        "clinic": "Example Clinic",
        "date": "11 Dec 2023",
        "time": "11:30 am"
    }
}
```
{% endcode %}

**CSV example for batch send**

{% code title="Example CSV for batch send" %}
```csv
recipient,language,name,clinic,date,time
6599999999,ENGLISH,John Doe,Example Clinic,11 Dec 2023,11:30 am
```
{% endcode %}

### **A**PI users who do not want to manage your message templates within Postman

If you are an API user that

* manages message templates within your own system
* uses Postman solely for sending out the full text of your message

you may create a single variable, `{{body}}`, and insert the message into the `{{body}}` variable.

<figure><img src="../.gitbook/assets/Screenshot 2024-01-09 at 3.19.35 PM (1).png" alt=""><figcaption></figcaption></figure>

**Request Body example - single variable `{{body}}`**

{% code title="Example Request body" %}
```
{
    "recipient": "6599999999",
    "language": "english",
    "values": {
    // The following values are values for the parameters in the example template
        "body": "Fill in your system constructed message here"
    },
}
```
{% endcode %}

**CSV example for batch send - single variable `{{body}}`**

{% code title="Example CSV for batch send" %}
```
recipient,language,body
6599999999,english,"Fill in your system constructed message here"
```
{% endcode %}

### Line breaks in \{{body\}} messages

When formatting line breaks in your request body, please note the differences between

1. [Single message](#user-content-fn-1)[^1]
2. [Batch messages](sending-messages-via-postman-api.md#batch-messages)

#### Single message

**Request Body example - `{{body}}` and line breaks**

{% code title="Example Request Body with line breaks" %}
```
{
    "recipient": "6599999999",
    "language": "english",
    "values": {
    // The following values are values for the parameters in the example template
        "body": "Dear Amy \n\nYour appointment for VACCINATION is confirmed.\n\nPlease do not reply to this message."
    },
}
```
{% endcode %}

For single message requests, you **will be required** to add the `\n` in your request body.

#### Batch messages

Postman only accepts .csv files for batch message. Take note of the differences when creating messages in excel and in a text editor.&#x20;

For batch messages, **do not** to use `\n` to create line breaks, as the characters will be read as plain text and get sent out to MOPs&#x20;

**Text Editor**

**CSV example for batch send - `{{body}}` and line breaks**

{% code title="Example Request Body with line breaks" %}
```
recipient,language,body
6591234567,english,"Dear Amy 

Your appointment for VACCINATION is confirmed.

Please do not reply to this message."
6599999999,english,"Dear John 

Your appointment for VACCINATION is confirmed.

Please do not reply to this message."
```
{% endcode %}

Your message in the `{{body}}` variable will need to be encased in `""` if you are creating messages from a text editor.

**Excel**

Excel automatically adds `""` to your file after you have saved it as a .csv file.

As such, **do not** encase the message in the `{{body}}` variable in `""`.

<figure><img src="../.gitbook/assets/Screenshot 2024-01-23 at 6.27.49 PM.png" alt=""><figcaption><p>Example of a CSV file</p></figcaption></figure>

### Postman Test Site limitations

{% hint style="danger" %}
**DO NOT** conduct load testing on our test site.&#x20;

[Postman test site](https://test.postman.gov.sg/) has a .csv file limit of 20 rows to ensure no load testing is done on this site. More information [here](../postman-v2-api-docs/about-postman-v2/postman-v2-slas.md#id-4.-whats-the-sms-throughput-rate) on load testing.
{% endhint %}

Postman's test site is meant for agency users to test out the platform. As such, you should test out the site like how you would send out messages to MOPs in a real scenario, where each number will only receive a single message.&#x20;

**Multiple messages to the same user**

If you send test messages with exact same content to the same person multiple times in 1 sitting in the same campaign:

eg. "Hi your appointment is on 1 Jan 2024" was sent to Tom 10 times within 1 batch send.

The telcos' automatic spam filter may be triggered . This means the message may not be delivered  to Tom's phone at all, even though it will pass Postman’s send filters and status is reflected as `delivered`.  See screenshot below on how the batch .csv is formatted in this failed example.

<figure><img src="../.gitbook/assets/image (39).png" alt=""><figcaption></figcaption></figure>

[^1]: 
