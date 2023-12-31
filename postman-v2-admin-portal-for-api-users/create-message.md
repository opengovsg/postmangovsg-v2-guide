# ✏ Create Message

## Sample Message

This is how your message will look like.

<figure><img src="../.gitbook/assets/Screenshot 2023-12-12 at 5.30.32 PM.png" alt=""><figcaption></figcaption></figure>

**Header**

The `Header` corresponds to the email account that you have logged into Postman with.

{% hint style="info" %}
If you have more than 1 official email address belonging to different agencies, ensure that you have [logged in with the correct email address](logging-into-postman-v2.md#singpass-login).
{% endhint %}

<div align="left">

<figure><img src="../.gitbook/assets/Screenshot 2023-12-20 at 2.57.15 PM.png" alt=""><figcaption></figcaption></figure>

</div>

If you need to change the agency in the `Header`, please contact us with your use case.

eg. You are helping to send messages on behalf of another agency.

## Message content

This flow allows you to create your own message in Postman using an editor and can be used by both admin portal and API users.

#### Variables

You will be able to create multiple `{{variables}}`. You can then input the values of each `{{variable}}`when you send the message from the admin portal or via API.

<figure><img src="../.gitbook/assets/Step 3_ Empty state - Gov.sg selected.png" alt=""><figcaption></figcaption></figure>

Variables have to fulfil the following in order to be successfully created

* Can only contain lowercase letters, numbers and `_`
* Must start with a lowercase letter
* If multiple languages are selected, the same variables must be present in all `language` tabs.

#### Language tab

If you are sending out messages in other languages, you can select the correct `language` tab before you key in your message content.

1. Message Content
   * Content in the message body field of each `language` is **not automatically translated.**
   * As a user, you will be required to input the correct language text into the message body field.
   * eg. If you select Malay as your `language`, you should input your message **in Malay** into the message body field; messages will not be translated for you.
2. SMS Footer
   * The SMS Footer of each message changes with the `language` selected.
   * eg. If you select Malay as your `language,` the SMS footer will change to Malay.

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
        "time": "11:30 am",
        "callback_link": "https://examplelink.gov.sg"
    }
}
```
{% endcode %}

**CSV example for batch send**

{% code title="Example CSV for batch send" %}
```csv
recipient,language,name,clinic,date,time,callback_link
6599999999,ENGLISH,John Doe,Example Clinic,11 Dec 2023,11:30 am,https://examplelink.gov.sg
```
{% endcode %}

### **A**PI users who do not want to manage your message templates within Postman

If you are an API user that

* manages message templates within your own system
* uses Postman solely for sending out the full text of your message

you may create a single variable, `{{body}}`, and insert the message into the `{{body}}` variable.

<figure><img src="../.gitbook/assets/Frame 12 (1).png" alt=""><figcaption></figcaption></figure>

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
6599999999,english,Fill in your system constructed message here
```
{% endcode %}
