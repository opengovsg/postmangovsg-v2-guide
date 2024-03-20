# Campaign related inquiries

1.  **Can campaigns be edited after creation?**

    *   No, they cannot be edited.

        If you need to edit your campaign’s message body, you will be required to create a new campaign.

        Users are now testing out campaigns on our test platform, and will have a fresh dashboard when they onboard onto our production site.
    * We will update the guide if there are any changes to this.&#x20;


2.  **If we have created multiple variables in a template, such as 4 variables, but we decide to only send 3 variables, is this allowed?**

    * No, you will need to pass provide details for all 4 variables. This applies to Postman API, SFTP and admin portal.


3.  **What is the maximum number of characters I can provide in each of the variables?**

    *   There is no limit on the number of characters in each variable. The total message length (excluding header and footer) shall not exceed 1000 characters. Please note that the character limit still applies to the characters within each variable.

        Refer to [this page](../../postman-v2-general-user-guide-mop/create-campaign/#character-count) for more information.


4.  **How many campaigns can I create, is there a limit?**

    * There is no limit, you can create as many campaigns as you want.


5.  **How do we know what is the `campaignID` ?**

    * Refer to our [API documents](https://api-docs.postman.gov.sg/campaigns-and-messages/create-campaign) for more information.


6.  **Are the creation of the templates/campaigns done through the Postman's web interface?**

    *   There will be no templates within the new Postman.

        Instead, there will be `campaigns` that can be created, and this will be done through Postman admin portal for all users - API, Admin portal and SFTP users. More information from our [API documents here](https://api-docs.postman.gov.sg/campaigns-and-messages/create-campaign).

        Upon the creating of a new campaign, a `campaignID` will be generated.


7. **Can we not set up any customised campaign - i.e. we can setup the API keys, IP whitelisting and starting using the Postman API to send out SMSes?**
   *   This is not possible as the API keys are tied to the campaign and can only be generated after a campaign is created.

       In such cases, we recommend creating a campaign with only [1 variable](../../postman-v2-admin-portal-for-api-users-mop/sending-messages-via-postman-api.md#api-users-who-do-not-want-to-manage-your-message-templates-within-postman) - `{{body}}`. You can then input any message body you wish from your own system into the `{{body}}` variable.
