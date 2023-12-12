# Create Message

Postman offers 2 types of template options for API users

### Option 1 - Simple messaging (Admin portal users and API users)

This option is selected when you turn on the `simple messaging` toggle.

It allows you to create your own message in Postman using an editor. You can use simple messaging to send messages via the Postman admin portal or Postman API. &#x20;

#### Variables

You will be able to create multiple `{{variables}}`. You can then input the values of each `{{variable}}`when you send the message from the admin portal or via API.&#x20;

<figure><img src="../.gitbook/assets/Option 1 (1) (2).png" alt=""><figcaption></figcaption></figure>

#### Language tab

If you are sending out messages in other languages, you can select the correct `language` tab before you key in your message content.&#x20;

1. Message Content
   * Content in the message body field of each `language` is **not automatically translated.**
   * As a user, you will be required to input the correct language text into the message body field.
   * eg. If you select Malay as your `language`, you should input your message **in Malay** into the message body field; messages will not be translated for you.&#x20;
2. SMS Footer
   * By selecting the language you want, this changes the SMS Footer of each message to the language selected.
   * eg. If you select Malay as your `language,` the SMS footer will change to Malay.

#### Request Body example&#x20;

```json
{
    "recipient": "+6599999999",
    "language": "english",
    "values": {
    // The following values are values for the parameters in the example template
        "name": "John Doe",
        "clinic": "Example Clinic",
        "date": "11 Dec 2023",
        "time": "11:30 am",
        "callback_link": "https://examplelink.gov.sg",
    },
}
```



### Option 2 - Advanced messaging (API Users only)

{% hint style="warning" %}
This feature should only be used by **advanced users** who will be constructing their messages from their own systems and not on the Postman admin portal.&#x20;



This option will cause the campaign to **lose its ability to send messages via the Postman admin portal.**
{% endhint %}

This option is selected when you turn off the `simple messaging` toggle.

#### Variables

You can only create messages with 1 fixed variable, `{{body}}`.&#x20;

<figure><img src="../.gitbook/assets/Option 2.png" alt=""><figcaption></figcaption></figure>

#### Language

1. Message Content
   * For API users, the `language` attribute will not affect your message content.
2. SMS Footer
   * The `language` attribute will only affect the SMS Footer. The footer will change into the `language` selected.&#x20;

#### Examples

Request Body example

```json
// Example Request Body for single send message
{
    "recipient": "+6599999999",
    "language": "english",
    "values": {
        // The following values are values for the parameters in the example template
        "body": "Fill in your system constructed message here"
    },
}
```

CSV example

<pre class="language-csv"><code class="lang-csv">// Example CSV for bulk send

<strong>recipient,language,body
</strong>+6599999999,ENGLISH,Fill in your system constructed message here
</code></pre>
