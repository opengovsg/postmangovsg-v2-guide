# Character count

### Character count

Postman's message character count is set at a **maximum of 1530 characters**, inclusive of the header and footer.&#x20;

As a precautionary measure, agencies are strongly advised to set their character count for each message body at **600 characters,** excluding the header and footer. A warning sign will appear for messages beyond 600 characters.&#x20;

Upon reaching 1000 characters (excluding header and footer), message sending will be disabled.

Message parameters alone i.e. `{{variable}}` do not count as characters. However, each populated message parameter adds towards overall character count. e.g. `{{name}}` is 0 characters, but `{{name}}` = `john` is 4 characters.

#### Message Blocks

Each message _block_ comprises of 160 characters. In Postman, a single **SMS** can comprise of more than 160 characters. The blocks will be combined and sent out as a single **SMS** to recipients. It is recommended that the body content of each SMS should not exceed 600 characters.&#x20;
