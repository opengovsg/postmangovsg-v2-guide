# Sending messages via SFTP

To send messages in bulk, you must prepare a CSV file where each column, in addition to `recipient` and `language`, represents a value corresponding to the campaign’s template parameter.

The examples below is based on the following campaign template:

{% hint style="info" %}
**The campaign template is configured on the admin portal during campaign creation**
{% endhint %}

{% code title="Example campaign template" %}
```bash
Dear {{recipient_name}},

This is to inform you that we have received your request for {{topic}}.

We will contact you again when we have processed your request. Thank you.
```
{% endcode %}



An example CSV file for the above template can be found below, along with an explanation of the various fields in the file.

{% code title="Example CSV file" %}
```
recipient,language,recipient_name,topic
6599999999,english,Emily Yeo,passport application #12345F
6599999998,chinese,James Tan,passport application #67890A
```
{% endcode %}

### **CSV file fields**

***

**recipient** string (Mandatory field)

For messages sent through the `sms` channel, the recipient will be the mobile phone number of the recipient, together with the country code of the recipient without including `+` in front.&#x20;

eg. `6591234567` is a recipient string for a Singapore (65) phone number (91234567)

***

**language** string (Mandatory field)

This is the language of the message template used to send this message.

This are the possible values `english`, `chinese`, `malay`, or `tamil`.

***

recipient\_name string (Optional field - depending on your message template content)

***

topic string (Optional field - depending on your message template content)

***



Subsequently, you will need to upload this file using the following command:

```bash
put <file to upload>
```

Please be aware that our system **does not generate output files**. The result of a file upload will be communicated to you via email. Once your field has been processed by our system, we will rename the file and append `.processed` to the file name.

Example:

If a user uploaded a file named `test-campaign.csv` , once our system has processed the file, it will be renamed to `test-campaign.processed.csv`.
