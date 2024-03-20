# API related inquiries

1.  **For 5XX server errors, will the requests be queued on Postman’s side?**

    * No.


2. **Regarding `Send messages in Bulk`, are there any limits on the number of messages that can be sent or on the file size?**
   *   Users can upload a CSV file of up to 30MB in size.

       The number of lines for this file size depends on the contents of your file.
3.  **If Postman is down, will there be a health check endpoint for agencies to check?**

    * No, but the team will be considering this point.


4.  **What's the typical and max time for a message latestStatus to move from `created` to `sent` to `success?` ?**

    *   As this is a brand new platform, the team does not have any data to release to agencies regarding typical and max time on the `latestStatus`.

        Note that the time taken for a message to be sent will also depend on the load at the point of creating and sending these messages.


5.  **How are SMS statuses charged?**

    * SMSes with a `failure` as the `latestStatus` will **not be charged**.


6.  **Do you provide a webhook for checking the status?**

    * No, that is not currently provided.


7.  **When do I use a Single Send API and when do I use a batch send?**

    *   Single Send API is used for when you need to send just one message out at a time.

        Batch message is when you have a single campaign and would like to broadcast the same message to many.

        If you use the Single Send API option but create too many request, you may encounter a 429 error.


8.  **If the bulk upload does not pass the validation check, can I proceed to send?**

    * No, the response will display row by row certain errors that need to be fixed before proceeding again.


9.  **Country Code Usage: If the country code, such as +65 for Singapore, is omitted, does Postman automatically assume it's intended for a Singapore number?**

    *   `65` is a mandatory field as Postman allows sending of messages overseas. The number will not be automatically assumed as a Singapore number if the country code is omitted.

        If the country code is omitted, the message will not be sent and a 4xx error will be reflected.


10. **Language Specification : If our template and values are in Chinese, but we specify English as the language, how will Postman behave?**

    * Scenario 1: You have removed `English` in the create campaign step, and specify `english` as a header in your .csv file. You will get an error informing you that you chose an unavailable language.&#x20;
    * Scenario 2: You have included `English` in the campaign creation step, but your message content is in chinese. Your message will have its message content in Chinese, but the footer will be in English. More information [here](https://api-docs.postman.gov.sg/campaigns-and-messages/create-message#language)[.](../../postman-v2-general-user-guide-mop/create-campaign/#language-tab)


11. **Language Parameter - Mandatory Field: Is the `language` parameter mandatory for sending messages?**

    * Yes.


12. **In the `Send single SMS` API, is it acceptable to transmit all content within the 'msg' under a value object?**

    1. Refer to the available options from our[ API documents](../../endpoints-for-api-users/single-send.md).


13. **For `latestStatus` field, how long do we need to wait before message is sent? How long to wait before we know if it was success or failure?**

    *   The response on whether the message was created will come in immediately. However, you will need to query `Retrieve message endpoint` to get the message `latestStatus`. Refer to our [API documents](https://api-docs.postman.gov.sg/endpoints-for-api-users/single-send) for more information.

        API users should call the GET status endpoint to retrieve the message status in real time.

        Alternatively, the delivery report with the sms status can be downloaded by the user from the Postman Admin Portal. This is a manual process and will not be automatically sent to the campaign admin’s email address.


14. **How do I reach out if I have any issues with my API integration or questions regarding the documents?**
    * Please fill up our [contact us form](https://form.gov.sg/admin/form/64a535b829d2650012a9938b), we aim to get back to you in 5 working days.
