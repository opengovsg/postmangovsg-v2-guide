---
description: >-
  We update this page regularly, please refer to API Documents latest updates
  for the last udpated date.
---

# ❓ Postman v2 SMS API FAQ

## General API docs questions

1.  **Can I share the API docs link with my vendors?**

    * Yes, please do so.


2. **Currently, we do API post with long SMS text content. Our SMS vendor will automatically split the message into several SMS messages to the end user. Is Postman the same?**
   * For long message content, it will be combined and will appear as a long message to the user.

## API keys generation and IP Address whitelisting

1.  **How can I obtain my API keys earlier for testing?**

    * You can now obtain your API keys on [test.postman.gov.sg](http://test.postman.gov.sg/). Read [here](https://api-docs.postman.gov.sg/postman-v2-api-docs/postman-v2-sms-api-user-documentation) for more information on calling Postman’s SMS API.


2.  **When can agencies test out the Postman API endpoints?**

    * You can now test Postman out on test.postman.gov.sg.


3.  **Regarding Authentication - can we have more information on bearer auth? Are we going to call a token API to get API keys or it will be generated from Postman Admin Portal?**

    * API keys are generated from the [Postman Admin Portal.](../postman-v2-admin-portal-for-api-users/create-campaign.md)


4.  **Does each agency get 1 API key for all systems or each system can request to get their separate unique API key?**

    * API keys are tied to each campaign, each campaigns can have up to 3 API keys. The number of keys will depend on the number of campaigns your agency has generated for your system.


5.  **What forms of authentication will you use for connecting via API?**

    * We will issue API keys via the Admin portal for each campaign. We will also whitelist IP addresses of each agency.


6.  **When do we submit our IP addresses for whitelisting?**

    * This will be done in the campaign creation flow. Refer to our [API documents](https://api-docs.postman.gov.sg/campaigns-and-messages/campaign-settings#ip-address-whitelisting) for more information.


7.  **Is whitelisting the source IP address sufficient for us to use Postman to send out SMSes?**

    * Yes. In addition, you will only be able to obtain your API keys **after** you have whitelisted your IP address.


8.  **Is there any firewall that we need to open to allow our API gateway to reach postman API gateway ?**

    * You will need to whitelist your IP addresses with us before you can obtain the API keys for integration.


9.  **Are the creation of the templates/campaigns done through the Postman's web interface?**

    * There will be no templates within the new Postman.
    * Instead, there will be `campaigns` that can be created, and this will be done through the Postman Admin Portal. More information from our [API documents here](../postman-v2-admin-portal-for-api-users/create-campaign.md).
    * Upon the creating of a new campaign, a `campaignID` will be generated.


10. **Can we not setup any customised campaign - i.e. we can setup the API keys, IP whitelisting and starting using the Postman API to send out SMSes?**

    * Not possible as the API keys are tied to the campaign and can only be generated after a campaign is created.
    * In such cases, we recommend creating a campaign [with only 1 variable - `{{body}}`](../postman-v2-admin-portal-for-api-users/create-message.md#api-users-who-do-not-want-to-manage-your-message-templates-within-postman). You can then input any message body you wish from your own system into the `{{body}}` variable.


11. **How do we know what is the `campaignID` ?**

    * Refer to our [API documents](https://api-docs.postman.gov.sg/campaigns-and-messages/create-campaign) for more information.


12. **How do we create templates/see the template details?**

    * We have amended the `curl` request, there should not be any `templates`.


13. **For 5XX server errors, will the requests be queued on Postman’s side?**

    * No.


14. **Regarding Batch Send, are there any limits on the number of** messages that can be sent or on the file size?

    * Users can upload a csv file of up to 20MB in size.
    * This translates to **approximately** 50,000 lines, depending on the contents of your file.


15. **If Postman is down, will there be a health check endpoint for agencies to check?**

    * No, but the team will be considering this point.


16. **What's the typical and max time for a message latestStatus to move from `created` to `sent` to `success?` ?**

    * As this is a brand new platform, the team does not have any data to release to agencies regarding typical and max time on the `latestStatus`.
    * Note that the time taken for a message to be sent will also depend on the load at the point of creating and sending these messages.


17. **How are SMS statuses charged?**

    * SMSes with a `failure` as the `latestStatus` will **not be charged**.


18. **Do you provide a webhook for checking the status?**

    * No, that is not currently provided.


19. **When do I use a Single Send API and when do I use a bulk send?**

    * Single Send API is used for when you need to send just one message out at a time. Bulk message is when you have a single campaign and would like to broadcast the same message to many.


20. **If the bulk upload does not pass the validation check, can I proceed to send?**

    * No, the response will display row by row certain errors that need to be fixed before proceeding again.


21. **How do we know what is the `campaignID` ?**

    * You can find it when you click into your campaign.


22. **Country Code Usage: If the country code, such as 65 for Singapore, is omitted, does Postman automatically assume it's intended for a Singapore number?**

    * `65` is a mandatory field as Postman allows sending of messages overseas. The number will not be automatically assumed as a Singapore number if the country code is omitted.
    * If the country code is omitted, the message will not be sent and a 4xx error will be reflected.


23. **Language Specification : If our template and values are in Chinese, but we specify English as the language, how will Postman behave?**

    * Your message will have its message content in Chinese, but your footer will be in English. More information [here](https://api-docs.postman.gov.sg/campaigns-and-messages/create-message#language).


24. **Language Parameter - Mandatory Field: Is the `language` parameter mandatory for sending messages?**

    * Yes


25. **In the `Send single SMS` API, is it acceptable to transmit all content within the 'msg' under a value object?**

    * Refer to the available options from our [API documents](https://api-docs.postman.gov.sg/campaigns-and-messages/create-message#language).


26. **If consolidating all content into one 'message' parameter is allowed, what is the maximum character limit for this parameter?**

    * \[Updated 18 Dec] 600 Characters


27. **For `LatestStatus` field, how long do we need to wait before message is sent? how long to wait before we know if it was success or failure?**

    * The response on whether the message was created will come in immediately. However, you will need to query `Retrieve message endpoint` to get the message `latestStatus`. Refer to our [API documents](https://api-docs.postman.gov.sg/endpoints-for-api-users/single-send) for more information.


28. **How do I reach out if I have any issues with my API integration or questions regarding the documents?**

    * Please fill up our [contact us form](https://form.gov.sg/admin/form/64a535b829d2650012a9938b), we aim to get back to you in 3 working days.
    * There willl be a technical training session conducted in January, please refer to the [Important Dates](../postman-v2-api-docs/important-dates.md) page for more information.


29. **What is Postman’s IP address?**
    * We do not provide our IP address, you can whitelist our domain name.&#x20;
    * If you really need our IP address, you can resolve the domain to find the IP address, but you will be responsible for updating it if it changes.&#x20;

## SFTP and Other integration methods

1.  **I heard that Postman will have SFTP integration. Are the documents ready?**

    * Please access our SFTP documents [here](https://api-docs.postman.gov.sg/sftp/sftp-integration).


2.  **When can I test out SFTP integration?**

    * End-Jan 2024.
    * SFTP interest form will only be released in End-Jan 2024.


3.  **Are there plans to provide SMPP to Postman integration?**

    * We are still consolidating agencies’ use cases and will inform agencies at a later date if this will be provided. If you have yet to provide your SMPP use case, fill up our request form [here](https://form.gov.sg/654c5f97a1058500113c1fef).


4. **Are there plans to provide SMTP to Postman integration?**
   * No.&#x20;
