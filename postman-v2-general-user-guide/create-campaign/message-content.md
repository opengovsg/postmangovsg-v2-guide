# Message content

## Message content

This flow allows you to create your own message in Postman using an editor and can be used by both admin portal and API users.

{% hint style="info" %}
For API users who do not want to manage your message templates within Postman, click [here](https://postman-v2.guides.gov.sg/postman-v2-admin-portal-for-api-users/create-message#api-users-who-do-not-want-to-manage-your-message-templates-within-postman) for more information.
{% endhint %}

### **Message parameters (variables)**

You can create multiple `{{variables}}` when typing out your message content. You can then input the values of each `{{variable}}`when you send the message from the admin portal or via API.

<figure><img src="../../.gitbook/assets/create_message (3).png" alt=""><figcaption></figcaption></figure>

Variables have to fulfil the following in order to be successfully created

* Can only contain lowercase letters, numbers and `_`
* Must start with a lowercase letter
* If multiple languages are selected, the same variables must be present in all `language` tabs.
