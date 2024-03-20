# 4. Configure Your Twilio Account

{% hint style="info" %}
You can only start configuring your Twilio account after you have completed the [setup](../3.-set-up-your-twilio-account.md).
{% endhint %}

You will first need to configure your Twilio account to ensure that it is functioning and is mapped to your Sender ID.&#x20;

Upon configuring your Twilio account, you will be able to obtain the necessary Twilio credentials required for you to input into your Postman campaign. More information can be found in [Step 6. Fill in your Twilio credentials in Postman](../6-fill-in-your-twilio-credentials-in-postman.md)

<figure><img src="../../../.gitbook/assets/Screenshot 2024-03-12 at 5.09.33 PM.png" alt=""><figcaption><p>Add your Twilio credentials into your Postman campaign</p></figcaption></figure>

### Take note of the credentials you'll need to save-keep to input into Postman: <a href="#before-you-start-note-the-credentials-youll-need-to-save-keep-to-input-into-postman" id="before-you-start-note-the-credentials-youll-need-to-save-keep-to-input-into-postman"></a>

1. [Account SID](./#id-1.-your-account-sid)
2. [API key SID](./#id-2.-api-key-sid)
3. [API Secret](./#api-secret) (_this is unretrievable once you proceed beyond this step, so make sure you have saved somewhere, or you will need to redo the set-up process to generate new keys_).
4. [Messaging Service ID](./#id-4.-message-service-id)

### 1. Account SID <a href="#id-1.-your-account-sid" id="id-1.-your-account-sid"></a>

An account SID is the unique identifier assigned to your agency account, much like an NRIC number. This is immediately available on your dashboard once you log into your account console.&#x20;

<figure><img src="../../../.gitbook/assets/Screenshot 2024-03-12 at 4.56.03 PM.png" alt=""><figcaption><p>Locate your account SID</p></figcaption></figure>

#### 1a. Account SID - Postman campaign settings

Insert your Account SID from your Twilio account console into Postman.&#x20;

<figure><img src="../../../.gitbook/assets/account SID (2).png" alt=""><figcaption></figcaption></figure>

### 2. API key SID

To set up your API key for Postman, select **`API keys & tokens`** on the side dashboard under **Accounts**.

<figure><img src="../../../.gitbook/assets/image (15).png" alt=""><figcaption><p>Select "API keys &#x26; tokens"</p></figcaption></figure>

Then, create a new **standard** API key by selecting `Create API key`.

<figure><img src="../../../.gitbook/assets/image (16).png" alt=""><figcaption><p>Select "Create API key"</p></figcaption></figure>

Create a `friendly name` for your API key so you can easily identify it in the future, and select `Standard` as the API key type.

<figure><img src="../../../.gitbook/assets/image (18).png" alt=""><figcaption><p>Name your API key, and set key type as "standard"</p></figcaption></figure>

You can find your API key under the Auth Tokens & API keys page.&#x20;

<figure><img src="../../../.gitbook/assets/image (19).png" alt=""><figcaption></figcaption></figure>

#### 2a. API Key SID - Postman campaign settings

Insert your API Key SID from your Twilio account console into Postman.&#x20;

<figure><img src="../../../.gitbook/assets/API Key SID.png" alt=""><figcaption></figcaption></figure>

### 3. API Secret

When creating your API key, a `secret key` associated with your API key will be shown.

Save your secret key

{% hint style="danger" %}
**Once you lose this secret key or if you do not save it, you will NOT be able to retrieve it again after moving on to the next step**
{% endhint %}

<figure><img src="../../../.gitbook/assets/image (20).png" alt=""><figcaption><p>Save the API key SID and Secret Key somewhere safe!</p></figcaption></figure>

{% hint style="danger" %}
Make sure you **copy and save** these details somewhere safe
{% endhint %}

Check the box and click `Done`.

#### 3a. API Secret - Postman campaign settings

Insert your API Secret Key from your Twilio account console into Postman.&#x20;

<figure><img src="../../../.gitbook/assets/API secret.png" alt=""><figcaption></figcaption></figure>

### 4. Message Service ID

This is the last detail you need to save before proceeding to Postman.

{% hint style="info" %}
There is no need to purchase a US phone number if your are sending messages **only** to Singapore numbers.
{% endhint %}

**If you are sending SMSes to foreign numbers,** you will still need to purchase a phone number at USD$1.15. Otherwise, your messages will not be delivered. Find out how to purchase a phone number [here](https://postman-v1.guides.gov.sg/campaign-guide-sms/onboarding-overview/step-4-configure-your-twilio-account/what-if-i-need-to-buy-a-phone-number), and follow these [steps](https://postman-v1.guides.gov.sg/campaign-guide-sms/onboarding-overview/step-4-configure-your-twilio-account/what-if-i-need-to-buy-a-phone-number) to set up your messaging service ID. You can ignore the steps below if you are purchasing a phone number.

**If you don't have a need to purchase a phone number, follow these steps to obtain your messaging service SID.**

Go back to your Twilio home page, and select `Set up a Messaging Service`.

<figure><img src="../../../.gitbook/assets/image (21).png" alt=""><figcaption></figcaption></figure>

On the side bar, click `Develop` > `Messaging` > `Services` > `Create Messaging Service.`

<figure><img src="../../../.gitbook/assets/image (22).png" alt=""><figcaption><p>Create your messaging service</p></figcaption></figure>

Name your messaging service and indicate the purpose. This will help you better identify your use cases, especially if you have multiple, and will also help Twilio detect your specific use case quicker should you need their help for troubleshooting.

<figure><img src="../../../.gitbook/assets/image (23).png" alt=""><figcaption><p>Fill in the required details</p></figcaption></figure>

**Set up your alphanumeric Sender ID**

Configure your alphanumeric Sender ID by selecting `Alpha Sender` under `Add Senders` > `Sender Type.`

<figure><img src="../../../.gitbook/assets/image (24).png" alt=""><figcaption><p>Select "Alpha Sender"</p></figcaption></figure>

Click `Continue`. _You may ignore the notification indicating that Alphanumeric Sender is not enabled for this account._

Specify the Alphanumeric Sender ID you want to use in the text box.&#x20;

{% hint style="info" %}
**It is best to align the Alphanumeric Sender ID with the Sender ID that you registered with SGNIC.**
{% endhint %}

<figure><img src="../../../.gitbook/assets/image (25).png" alt=""><figcaption><p>Add in your Sender ID</p></figcaption></figure>

**If the Alphanumeric Sender ID you chose is protected,** you will notice either of the two things below.

* You encounter an error when setting it up on the Sender Pool page
* You may not receive any message when you send a test SMS

This also means that this Sender ID has been registered by another entity and you will not be able to use it.

Once you have completed the step above, you may click the `Skip Setup` button below.

<figure><img src="../../../.gitbook/assets/image (26).png" alt=""><figcaption><p>Complete the set up</p></figcaption></figure>

After clicking "Skip setup" in the step above, you should be brought to the Properties page of this Messaging Service.&#x20;

On this page, you should be able to find the **Messaging Service ID**.

<figure><img src="../../../.gitbook/assets/image (27).png" alt=""><figcaption><p>This is your messaging service SID</p></figcaption></figure>

#### 4a. Message Service ID - Postman campaign settings

Insert your Messaging Service SID into Postman.&#x20;

<figure><img src="../../../.gitbook/assets/Messaging Service ID.png" alt=""><figcaption></figcaption></figure>

