# Delivery Report

1.  **Will specific error codes be shown for SMS failures?**

    * Yes, it will be in the delivery report that can be downloaded for each campaign. This will come in the form of a CSV file all messages ever sent for the batch or campaign. You should filter for the desired month within the CSV file itself.


2.  **How long will campaign logs be retained for?**

    * They are stored indefinitely.


3.  **If a message is sent out in a batch and has an error, will there be individual error logs for the messages that failed to send?**

    *   Yes, individual error logs will be available.

        The messages in the batch will be sent out except for those that have failed.


4.  **Are there any differences between Postman v1 and Postman v2**

    * The original Postman (now named “Postman v1”) will only serve the function of sending emails. Public healthcare institutions can still use Postman v1 to send SMSes. You may access Postman v1 via [https://postman.gov.sg/](https://postman.gov.sg/)
    * The new Postman (”Postman v2”) will give users the functionalities of sending SMSes to MOP using the `gov.sg` sender ID, or to internal staff using their own registered sender IDs. All other government agencies should use Postman v2 for SMS sending through `gov.sg` or to internal staff. You may access Postman v2 test site via [https://test.postman.gov.sg/](https://postman.gov.sg/)


5. **If messages fail to be delivered, will they be charged?**
   * No.
