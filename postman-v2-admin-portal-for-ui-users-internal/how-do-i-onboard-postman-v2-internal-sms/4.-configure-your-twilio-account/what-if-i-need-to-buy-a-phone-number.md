# What if I need to buy a phone number?

Phone number purchase is necessary if you are sending SMSes to **foreign numbers**. Follow the steps here to purchase a number.

{% hint style="danger" %}
This step must be done before setting up your messaging service ID
{% endhint %}

### How to buy a phone number?

On the left console, select `Develop > Phone Numbers > Manage > Buy a number.`

<figure><img src="../../../.gitbook/assets/image (29).png" alt=""><figcaption></figcaption></figure>

Select the phone number that you prefer.

<figure><img src="../../../.gitbook/assets/image (30).png" alt=""><figcaption><p>Buy your number</p></figcaption></figure>

#### How to set up messaging service ID with phone number? <a href="#how-to-set-up-messaging-service-id-with-phone-number" id="how-to-set-up-messaging-service-id-with-phone-number"></a>

You need to create a messaging service and tie the phone number that you bought to this messaging service before you can send SMSes.

Go back to your Twilio home page, and select`Set up a Messaging Service`.

<figure><img src="../../../.gitbook/assets/image (31).png" alt=""><figcaption></figcaption></figure>

On the side bar, click `Develop > Messaging > Services > Create Messaging Service.`

<figure><img src="../../../.gitbook/assets/image (37).png" alt=""><figcaption><p>Create your messaging service</p></figcaption></figure>

Name your messaging service and indicate the purpose. This will help you better identify your use cases if you have multiple, and will also help Twilio detect your specific use case quicker should you need their help for troubleshooting.

<figure><img src="../../../.gitbook/assets/image (32).png" alt=""><figcaption></figcaption></figure>

Add your `Sender Pool`. Sender Pool is where you configure the sender details such as the phone number you bought, and input your alphanumeric Sender ID.

Click `Add Senders.`

<figure><img src="../../../.gitbook/assets/image (33).png" alt=""><figcaption><p>Set up sender pool</p></figcaption></figure>

Add the phone number you purchased to this service.

<figure><img src="../../../.gitbook/assets/image (34).png" alt=""><figcaption><p>Select <code>Phone Number</code></p></figcaption></figure>

Select the number you want to associate with this messaging service (if you have more than one).

<figure><img src="../../../.gitbook/assets/image (35).png" alt=""><figcaption><p>Select desired number</p></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (36).png" alt=""><figcaption><p>Number selected successfully</p></figcaption></figure>

Then, go back [here](./#id-4.-message-service-id) to continue the set-up of your alphanumeric Sender ID.
