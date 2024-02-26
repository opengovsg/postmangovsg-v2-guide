# Message Statuses

1.  **What's the typical and max time for a message latestStatus to move from `created` to `sent` to `success?` ?**

    * As this is a brand new platform, the team does not have any data to release to agencies regarding typical and max time on the `latestStatus`.
    * Note that the time taken for a message to be sent will also depend on the load at the point of creating and sending these messages.


2.  **How are SMS statuses charged?**

    * SMSes with a `failure` as the `latestStatus` will **not be charged**.


3.  **Do you provide a webhook for checking the status?**

    * No, that is not currently provided.


4.  **For `LatestStatus` field, how long do we need to wait before message is sent? How long to wait before we know if it was success or failure?**

    * The response on whether the message was created will come in immediately. However, you will need to query `Retrieve message endpoint` to get the message `latestStatus`.&#x20;
    * We also currently do not support pushing delivery status to your server via webhooks when the status of a message changes.&#x20;
    * Refer to our [API documents](https://api-docs.postman.gov.sg/endpoints-for-api-users/single-send) for more information.


5.  **Will Postman retry sending failed messages automatically?**

    * No, you will need to manually re-send the failed messages.


6. **How can I check if the message has been read by the recipient?**
   * Telcos do not provide read statuses. Please see the list of available statuses [here](https://postman-v2.guides.gov.sg/endpoints-for-api-users/the-message-object#lateststatus-string).
