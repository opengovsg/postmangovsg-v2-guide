---
description: How do I download message logs for my campaign?
---

# 🪵 Message Logs

In the campaign dashboard, there are 2 categories:

1. [Messages](message-logs.md#messages)
2. [Batches](message-logs.md#batches)

### Messages

Messages consists of all messages that you have sent out in a single campaign.&#x20;

Messages may be sent out as a single message, or can be part of a batch of messages. You may identify this through the `Job Type` column in the campaign dashboard.

_(Please ignore the details under From column.)_

<figure><img src="../.gitbook/assets/campaign dashboard general (1).png" alt=""><figcaption></figcaption></figure>

In order to download the message logs for this campaign, please click on the <img src="../.gitbook/assets/Screenshot 2024-02-26 at 2.54.22 PM.png" alt="" data-size="line">icon on the screen.

<figure><img src="../.gitbook/assets/campaign logs single.png" alt=""><figcaption></figcaption></figure>

You will then receive the logs in your email, and you may filter out the required logs you will need using excel.

Each message will have its own message ID, this message ID can be found in the message logs that you download.&#x20;

### Batches

A batch consists of multiple messages that are sent out at the same time. Each batch will come with its own Batch ID, and each batch can be downloaded by clicking on the <img src="../.gitbook/assets/Screenshot 2024-02-26 at 2.54.22 PM.png" alt="" data-size="line"> icon tagged to each batch.&#x20;

<figure><img src="../.gitbook/assets/batch copy.png" alt=""><figcaption></figcaption></figure>

Similarly, you will receive the logs in your email, and you may filter out the required logs you will need using excel.

### Retrieving logs by calling Postman API endpoints

Refer to the following pages to retrieve the message status for your campaigns

* [Retrieve Message](message-logs.md#messages)
* [Retrieve Batch](message-logs.md#batches)
