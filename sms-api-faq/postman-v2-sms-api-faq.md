---
description: >-
  This page is still under development, please check back periodically for new
  questions and updates.
---

# Postman v2 SMS API FAQ

1. **How do we create templates/see the template details?**\
   We have amended the`curl` request that was previously published; there should not be any `templates`.\

2. **Are the creation of the templates/campaigns done through the Postman’s web interface?**\
   There will be no templates within the new Postman.\
   Instead, there will be `campaigns` that can be created, and this will be done through the Postman admin portal (Postman UI).\
   Upon the creating of a new campaign, a `campaignID` will be generated.\
   We will release this part of the document once the staging platform is up.\

3. **What forms of authentication will you use for connecting via API?**\
   We will issue API keys via the Postman admin portal for each campaign. We will also whitelist IP addresses of each agency.\

4. **When can agencies test out the Postman UI?**\
   Our staging platform will be up by the end of December 2023, where agencies can test out the new platform and obtain API keys needed for testing.\

5. **For 5XX server errors, will the requests be queued on Postman’s side?**\
   No.\

6. **Regarding** [**Send messages in Bulk**](https://docs.developer.tech.gov.sg/docs/postman-sgdp-guide/send-messages-in-bulk) **are there any limits on the number of messages that can be sent or on the file size?**\
   Users can upload a csv file of up to 20MB in size.\
   This translates to **approximately** 50,000 lines, depending on the contents of your file.\

7. **If Postman is down, will there be a health check endpoint for agencies to check?**\
   No, but the team will be considering this point.\

8. **What’s the typical and max time for a message latestStatus to move from `created` to `sent` to `success`?**\
   As this is a brand new platform, the team does not have any data to release to agencies regarding typical and max time on the `latestStatus`.\
   Note that the time taken for a message to be sent will also depend on the load at the point of creating and sending these messages.\

9. **How are SMS statuses charged?**\
   SMS-es with a `failure` as the `latestStatus` will **not be charged**.\

10. **Do you provide a webhook for checking the status?**\
    No, that is not currently provided.\

11. **When do I use a Single Send API and when do I use a bulk send?**\
    Single Send API is used for when you need to send just one message out at a time.\
    Bulk message is when you have a single campaign and would like to broadcast the same message to many.\

12. **If the bulk upload does not pass the validation check, can I proceed to send?**\
    No, the response will display row by row certain errors that need to be fixed before proceeding again.\
