---
description: Postman's internal SMS set up is exactly the same as Postman Legacy SMS set up
---

# Internal SMS

Postman v2 connects with Twilio to send out messages within the agency.&#x20;

### What is the difference between Twilio and Postman? <a href="#what-is-the-difference-between-twilio-and-postman" id="what-is-the-difference-between-twilio-and-postman"></a>

Postman is a free multi-channel communications platform built by Open Government Products for all public service agencies. Postman provides a convenient interface for you to craft your message, upload your recipient list, and send your campaign. Using Postman itself is free.

Twilio is a commercial cloud communication service that allows users to send messages (including SMS) through an Application Program Interface (API). Twilio bills users directly for its services; in this case, any SMSes you send using the Postman interface will be billed to you directly by Twilio. Postman does not pay for the SMSes that you send, but neither does Postman charge you for sending SMSes using our interface.

### Why Twilio? <a href="#why-twilio" id="why-twilio"></a>

We evaluated other cloud-based SMS service providers like Nexmo and AWS SNS before we chose Twilio. We chose Twilio for its simple user interface with an interactive debugger. Its API documentation is also well written, and its API easy to set up. The API also optimises the rate limit to send bulk messages, and allow for users to retry for messages with errors during the first attempted delivery.

Importantly, Twilio API's success rate is 99.999% & uptime is around 99.95% monthly.

Since inception, we have used Twilio for SMS sending services, such as NDP ticketing, Digital MCs, SGH's elective surgery appointment reminders, and quarantine ops by MOH and ICA during Covid-19.

### Can I trial using Postman to send SMSes before deciding whether to onboard onto Twilio? <a href="#can-i-trial-using-postman-to-send-smses-before-deciding-whether-to-onboard-onto-twilio" id="can-i-trial-using-postman-to-send-smses-before-deciding-whether-to-onboard-onto-twilio"></a>

Unlike Postman Legacy, Postman v2 does not offer users accounts with free demo campaigns.&#x20;

You will need to have valid Twilio credentials, put them in Postman, and use this to send SMSes. You can send test SMSes to your own phone number, but this will be charged to your Twilio account directly.
