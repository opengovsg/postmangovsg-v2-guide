# API keys generation and IP Address whitelisting

1.  **How do we know what is the `campaignID` ?**

    * Refer to our [API documents](https://api-docs.postman.gov.sg/campaigns-and-messages/create-campaign) for more information.


2.  **How can I obtain my API keys earlier for testing?**

    * You can now obtain your API keys on [test.postman.gov.sg](http://test.postman.gov.sg/). Read [here](https://api-docs.postman.gov.sg/postman-v2-api-docs/postman-v2-sms-api-user-documentation) for more information on calling Postman’s SMS API.


3.  **When can agencies test out the Postman API endpoints?**

    * You can now test Postman out on test.postman.gov.sg.


4.  **Regarding Authentication - can we have more information on bearer auth? Are we going to call a token API to get API keys or it will be generated from Postman Admin Portal?**

    * API keys are generated from the [Postman Admin Portal.](../../postman-v2-general-user-guide-mop/create-campaign/)


5.  **Does each agency get 1 API key for all systems or each system can request to get their separate unique API key?**

    * API keys are tied to each campaign, each campaigns can have up to 3 API keys. The number of keys will depend on the number of campaigns your agency has generated for your system.


6.  **What forms of authentication will you use for connecting via API?**

    * We will issue API keys via the Admin portal for each campaign. We will also whitelist IP addresses of each agency.


7.  **When do we submit our IP addresses for whitelisting?**

    * This will be done in the campaign creation flow. Refer to our [API documents](https://api-docs.postman.gov.sg/campaigns-and-messages/campaign-settings#ip-address-whitelisting) for more information.


8.  **Is there any firewall that we need to open to allow our API gateway to reach postman API gateway ?**

    * You will need to whitelist your IP addresses with us before you can obtain the API keys for integration.


9.  **Is whitelisting the source IP address sufficient for us to use Postman to send out SMSes?**

    * Yes. In addition, you will only be able to obtain your API keys **after** you have whitelisted your IP address.


10. **What is Postman’s IP address?**

    * We do not provide our IP address, you can whitelist our domain name.&#x20;
    * If you really need our IP address, you can resolve the domain to find the IP address, but you will be responsible for updating it if it changes.&#x20;


11. **For 5XX server errors, will the requests be queued on Postman’s side?**
    * No.
