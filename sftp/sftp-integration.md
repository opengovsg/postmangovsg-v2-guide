# 📂 SFTP Integration

SFTP integration for campaigns is exclusively available on an opt-in basis and is not accessible through the admin portal.&#x20;

* For questions related to SFTP, you may submit your inquiries [here](https://form.gov.sg/657025a2d2bd350012c82eb0).&#x20;
* For agencies interested to use SFTP, this option is **not available** at the moment and the interest form will only be released in **2024.**&#x20;



Please provide the following details in the respective interest form:

| Environment            | Form Link  |
| ---------------------- | ---------- |
| Test Environment       | tbc        |
| Production Environment | tbc        |
|                        |            |

* SSH public key&#x20;
  * We will use this to verify their SSH private key when they attempt to connect to the SFTP server
  * Refer to the following guide for instructions on generating ssh keys: [SSH Key Generation Guide](https://docs.oracle.com/en/cloud/cloud-at-customer/occ-get-started/generate-ssh-key-pair.html#GUID-8B9E7FCB-CEA3-4FB3-BF1A-FD3406A2432F)
* Campaign ID : campaign which needs SFTP integration
  * Users are required to first create a campaign through the admin portal
* Campaign API Key&#x20;
  * API key of the campaign
  * This can be generated from the Settings -> Integrations Tab
  * Do not that you would have to whitelist these 2 static IP addresses per campaign
    * NOTE: IP address will be provided from Feb 2024 onwards
* Notification Email
  * The notification email we will use to send the result of the file upload to

Once done, we will be providing you

* username&#x20;
  * Username to use for connecting to SFTP server&#x20;
  * The username will be your `campaignId`
* sftp server ip
  * Two static IPs for connecting to the SFTP server (environment dependent)
