# Messaging

1.  **Will there be a monthly report with a CSV file containing all the SMS sent for the month? Will it be emailed to us?**

    *   The delivery report can be downloaded directly from Postman by the user. This will come in the form of a CSV file all messages ever sent for the batch or campaign. You should filter for the desired month within the CSV file itself.

        The is applicable for both admin portal and API users.

        Additionally, API users can also call the [GET status endpoint](../../endpoints-for-api-users/retrieve-message.md) to retrieve message status in real time.


2.  **Can agencies use Postman for both external and internal messages?**

    * Yes. The Sender ID for SMS to external MoPs will be '[gov.SG](http://gov.sg)' and SMS to internal staff will be your own agency-registered sender ID.


3.  **What is the maximum length of the message in the SMS? We may need to include clickable links.**

    * Please refer to [character count](https://postman-v2.guides.gov.sg/postman-v2-admin-portal-for-api-users/create-message#message-content).


4.  **Usually, the message count for 1 sms is 160 characters. For the new format, are the header and footer counted as SMS characters?**

    * Yes, it will be counted. When recipients receive the messages, the character blocks will be combined to form a single message.


5.  **Can I change the header of my Agency name?**

    * No except for the following cases
      1. you are sending messages on behalf of another agency.
      2. your product sends out messages on behalf of various agencies.
    * For such cases, please contact us [here](https://form.gov.sg/657025a2d2bd350012c82eb0).


6.  **What is the sender ID on your test site?**

    *   The sender ID on our test site is `Postman`.

        Your agency’s sender ID will be available for use on our production site, refer to our guide for more details.


7.  **My agency is currently using Postman v1. Do I need to switch over to using Postman v2?**

    * Yes, unless you’re from a public healthcare institution.


8.  **How many SMSes can I trigger per day, are there restrictions?**

    * No restrictions, however, please note
      * differences between batch and single send
      * the batch size requirements
    * or you may encounter a 429 error.


9.  **If the messages are sent out unsuccessfully, will there be an automatic retry from Postman’s end?**

    * No, you will need to call our endpoints again as this will not be automatically done. UI users will need to re-send from the portal.


10. **Is there a separate queue for time sensitive messages?**
    * No.
