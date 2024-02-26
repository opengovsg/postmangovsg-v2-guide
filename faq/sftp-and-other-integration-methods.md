# 🗃️ SFTP and Other integration methods

1.  **I heard that Postman will have SFTP integration. Are the documents ready?**

    * Please access our SFTP documents [here](https://api-docs.postman.gov.sg/sftp/sftp-integration).


2.  **Are there plans to provide SMPP to Postman integration?**

    * We will release our SMPP integration details on 1 April 2024


3.  **Are there plans to provide SMTP to Postman integration?**

    * No.&#x20;


4. **Can we send encrypted files via SFTP?**
   * No, the files need to be in csv format
5.  **For SFTP, when will the SMSes be sent and when should the files be deposited?**

    * They are sent out in real time upon Postman receiving the files from agencies.


6.  **What if the test environment cannot handle my production load**

    1. You should not be using postman to conduct load testing. Please refer to [this page](../postman-v2-api-docs/about-postman-v2/postman-v2-slas.md#id-4.-whats-the-sms-throughput-rate) for more information.


7. **Will load testing be available on Postman test and production sites?**
   * Load testing on Postman will only be available a separate site, **not the test site**. Please refer to [this page](../postman-v2-api-docs/about-postman-v2/postman-v2-slas.md#id-4.-whats-the-sms-throughput-rate) for more information.
   * You will need to complete load testing on your own system’s end, to ensure that your system is able to handle the load you will be sending over to our end.
   * Please also ensure that you are using the correct method to send your messages (single send vs batch send), as you may receive a `429` error if Postman receives too many request too quickly.

{% hint style="danger" %}
Please **do not** conduct load testing on our test site. We will proceed to remove your API keys if we noticed that load testing was done on our test site.
{% endhint %}
