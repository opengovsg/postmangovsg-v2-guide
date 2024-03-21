# Information for new Twilio users

<table><thead><tr><th width="206">Topic</th><th>Details</th></tr></thead><tbody><tr><td><a href="https://support.twilio.com/hc/en-us/articles/115002943027-Understanding-Twilio-Rate-Limits-and-Message-Queues">Send Rate</a></td><td>SMSes are sent by Twilio at a default of 10 messages per second. </td></tr><tr><td>SMS character <a href="https://www.twilio.com/docs/glossary/what-sms-character-limit">limit</a></td><td><p>Each message segment is capped at <strong>160 characters</strong>. </p><p></p><p>Beyond this character limit, the single SMS will consist of 2 or more message segments, depending on the length of your SMS. </p><p></p><p>You will be charged at a <strong>per-message-segment rate</strong>.</p></td></tr><tr><td>Resources</td><td><p></p><p>Each agency/department will need its own Twilio account set up before SMSes can be sent via Postman. </p><p></p><p>This is for billing and governance purposes. </p><p></p><p>Not to worry - we will guide you through the set up of this account!</p><p><br></p></td></tr><tr><td>Maximum number of SMSes</td><td><p></p><p>There is no limit to how many SMSes or recipients you can send using Postman's interface. Our record is 144,000 SMSes sent in 1 batch by a government agency.</p></td></tr><tr><td>1-way SMS</td><td>Postman only allows for sending of 1-way messages. <br><br>This means that agencies can send mass SMSes to recipients using Postman, but there is currently no functionality on Postman for you to receive any responses that your recipients might send.</td></tr></tbody></table>

### Billing and Costs <a href="#billing-and-costs" id="billing-and-costs"></a>

Twilio works on a pre-payment method - you will need to top up your account with credits before SMSes can be sent. [Recharge triggers](https://support.twilio.com/hc/en-us/articles/223135607-How-do-I-set-a-recharge-or-notification-trigger-) can be set so that you don't have to manually top up these credits.

Billing is generally done using a _**corporate credit card**._ Read more about Twilio's billing methods [here](https://support.twilio.com/hc/en-us/articles/360042138913-Payment-Options-for-Twilio-Invoices).

If you are unable to obtain a corporate credit card, you can explore direct invoicing with Twilio. However, Twilio requires a minimum spend of US12,000 annual (or about 25,000 SMSes per month) to qualify for this mode of payment.

### **What is the cost?**

At this point of writing (March 2024), it costs USD$0.0415 per message segment of 160 characters to send to recipients with Singapore numbers. If your message is longer than 160 characters, you will be charged the cost of as many message segments.

You may refer to Twilio's [page](https://www.twilio.com/sms/pricing/sg) for the latest rates. You will be charged the cost according to the destination handset i.e. you will be charged the US rate for sending to a US number, even if the recipient with this number is based in Singapore.
