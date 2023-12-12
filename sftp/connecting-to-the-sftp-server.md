# Connecting to the SFTP server

Upon completion of the SFTP integration, we will furnish you with the `ipAddress` for the SFTP server. Users will use their `campaignId` as their username to access the server.

A connection to our SFTP server can be established by executing the following command:

```bash
sftp -i <user's ssh private key> campaignId@ipAddress
```
