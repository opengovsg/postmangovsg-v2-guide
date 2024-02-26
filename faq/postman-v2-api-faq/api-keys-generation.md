# API keys generation

1.  **How can I obtain my API keys earlier for testing?**

    * You can now obtain your API keys on [test.postman.gov.sg](http://test.postman.gov.sg). Read [here](https://api-docs.postman.gov.sg/postman-v2-api-docs/postman-v2-sms-api-user-documentation) for more information on calling Postman’s SMS API.


2.  **When can agencies test out the Postman API endpoints?**

    * You can now test Postman out on [test.postman.gov.sg](http://test.postman.gov.sg).


3.  **Regarding Authentication - can we have more information on bearer auth? Are we going to call a token API to get API keys or it will be generated from Postman? Admin Portal?**

    * API keys are generated from the [Postman Admin Portal](https://api-docs.postman.gov.sg/).


4.  **Does each agency get 1 API key for all systems or each system can request to get their separate unique API key?**

    * API keys are tied to each campaign. Each campaign can have up to 3 API keys. The number of keys will depend on the number of campaigns your agency has generated for your system.


5. **What forms of authentication will you use for connecting via API?**
   * We will issue API keys via Postman for each campaign. We will also whitelist IP addresses of each agency. Users are required to input their IP addresses for whitelisting, and obtain their API keys within Postman. Read [here](https://api-docs.postman.gov.sg/postman-v2-admin-portal/campaign-settings#integrations-ip-address-whitelisting) for more info.
