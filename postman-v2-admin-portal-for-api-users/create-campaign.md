---
description: How do I start creating a campaign?
---

# 📢 Create Campaign

{% hint style="warning" %}
Campaign creators **must** log in with their `.gov.sg` email address. \
Users with no `.gov.sg` email address are **not allowed** to create campaigns.&#x20;
{% endhint %}

In order to obtain your API keys for system integration, you will need to&#x20;

1. Create Campaign and obtain a Campaign ID
2. [Whitelist your IP address](campaign-settings.md#ip-address-whitelisting)
3. [Generate your API keys](campaign-settings.md#api-keys)

## Home page

To start creating campaigns, select  `+ Create campaigns` on your home page

{% hint style="info" %}
Please ignore `TODO: Persist sender ID` under the `Sender ID` field.
{% endhint %}

<figure><img src="../.gitbook/assets/home_create_campaign (2).png" alt=""><figcaption></figcaption></figure>

### Create Campaign

You will be taken to the `Create Campaign` page and asked to name your campaign

<figure><img src="../.gitbook/assets/create_name_campaign.png" alt=""><figcaption></figcaption></figure>

### Available channels for campaign creation

Postman has 2 types of campaign channels available - **Member of Public** and **Internal Staff**

<figure><img src="../.gitbook/assets/Campaign_create_updated (1).png" alt=""><figcaption><p>Available Channels</p></figcaption></figure>

1. Member of Public: To send out messages to MOPs
2. Internal Staff - to send out with your own sender ID
   * You will need to provide your own Twilio credentials if you choose the `Internal Staff` option

#### Temporary Sender Name (mid-April 2024 to launch)

Postman will be ready for use from mid-April 2024.&#x20;

Users will be able to use WOG Sender IDs that their agency have been registered with SGNIC thus far. The sender IDs will appear as options under the `Select temporary sender name` field.



In the example below, the available sender IDs that the user's agency has registered are `Government Technolocy Agency` and `Open Government Products`. The user willl not be able to see other sender IDs registered by other agencies.&#x20;

<figure><img src="../.gitbook/assets/Campaign_crete_temporary_sender_name.png" alt=""><figcaption><p>Available temporary sender IDs</p></figcaption></figure>

### Campaign content

You will be prompted to type out your message content.&#x20;

Click here for more information regarding [\{{variables\}}](create-message.md#variables).

<figure><img src="../.gitbook/assets/create_message (4).png" alt=""><figcaption></figcaption></figure>
