---
description: How do I use the admin portal (Postman UI) to send out messages?
---

# 📤 Sending messages via the Admin Portal

To start sending out messages, select the campaign that you wish to use. This will take you to the campaign dashboard page. You may choose to send to a single recipient or multiple recipients

<figure><img src="../.gitbook/assets/campaign compose.png" alt=""><figcaption></figcaption></figure>

### Single recipient

Upon selecting `single recipient`, a pop-up will prompt you to key in your recipient's details.

* Recipient's phone number
* Message language\*
* Message parameters

Once the details have been filled in, click `send` to send out your message.&#x20;

{% hint style="info" %}
Message language option is only available if the campaign admin has selected multiple languages during the [campaign creation process](../postman-v2-general-user-guide/create-campaign/#language-tab). If no languages have been added, the default language will be `English` and you will not be able to select other languages.&#x20;
{% endhint %}

{% hint style="info" %}
All message parameters needs to be filled before you can send out the message.
{% endhint %}

<figure><img src="../.gitbook/assets/Screenshot 2024-02-26 at 12.53.35 PM.png" alt=""><figcaption><p>Populate the required fields</p></figcaption></figure>

### Multiple recipients

Upon selecting multiple recipients, you will be prompted to upload a .csv file containing

* [recipient](sending-messages-via-the-admin-portal.md#recipient)
* [language](sending-messages-via-the-admin-portal.md#language)
* message parameters

{% hint style="info" %}
All message parameters need to be filled before you can send out your messages.
{% endhint %}

We highly recommend the following steps when formatting your .csv file to send out messages

1. Download campaign .csv template
2. Edit the .csv template and save it as a .csv file
3. Upload your .csv file

<figure><img src="../.gitbook/assets/multiple recipients (1).png" alt=""><figcaption><p>Step 1 and 3: Postman admin portal</p></figcaption></figure>

<figure><img src="../.gitbook/assets/Screenshot 2024-02-26 at 1.38.03 PM.png" alt=""><figcaption><p>Step 2: Edit .csv file - the header row will be automatically populated based on the message parameters input in the message template</p></figcaption></figure>

In the multiple recipients sending format, any errors in the CSV file rows will result in failure to send all other messages in the campaign. You will need to fix the error(s) before all messages in the batch can be sent.

The header row will require to match the [variables](../postman-v2-general-user-guide/create-campaign/#message-parameters-variables) created, such as containing lowercase letters, numbers and `_`.

#### Recipient

This contains mobile phone number of the recipient, prefixed by the country code but without the leading `+`. For example, when sending to a Singapore phone number, the value of recipient will be `6599999999.`

eg. `6591234567` is a recipient string for a Singapore (65) phone number (91234567)

#### Language

This column will need to be filled, even if there is only one available language that can be selected.

eg. If `English` is the only language you can choose in your message creation, you will need to fill every single entry with `English`.

### Postman Test Site limitations

Postman's test site is meant for agency users to test out the platform. As such, you should test out the site like how you would send out messages to MOPs in a real scenario, where each number will only receive a single message.&#x20;

If you send test messages with exact same content to the same person multiple times in 1 sitting in the same campaign:

eg. "Hi your appointment is on 1 Jan 2024" was sent to Tom 10 times within 1 batch send,

The telcos' automatic spam filter may be triggered . This means the message may not be delivered  to Tom's phone at all, even though it will pass Postman’s send filters and status is reflected as `delivered`.  See screenshot below on how the batch .csv is formatted in this failed example.

<figure><img src="../.gitbook/assets/Screenshot 2024-02-26 at 1.55.33 PM.png" alt=""><figcaption></figcaption></figure>
