# 📂 SFTP Integration

SFTP integration for campaigns is exclusively available on an opt-in basis and is not accessible through the admin portal.&#x20;

* For questions related to SFTP, you may submit your inquiries [here](https://form.gov.sg/657025a2d2bd350012c82eb0).&#x20;
* For agencies interested to use SFTP, follow the steps below, then submit this [form](https://go.gov.sg/sftp-interest-form).

### Beginning your SFTP integration

{% hint style="warning" %}
We only accept RSA, ECDSA, and ED25519 keys.
{% endhint %}

1. Log into Postman and create a new campaign
   * this generates your campaign ID needed to fill in the form
2. Generate your campaign API key
   * this is the API key associated with your campaign
   * find this in Settings -> Integrations
   * whitelist these two static IP addresses (note: there is no need to whitelist your SFTP client's IP addresses. You will just need to whitelist Postman's IP addresses below)

<table><thead><tr><th>Environment</th><th width="235">IP Address to Whitelist</th><th data-type="number">Port</th><th>SFTP Server Domain</th></tr></thead><tbody><tr><td>Test Environment</td><td>18.136.33.127, 52.77.196.100</td><td>22</td><td>test.sftp.postman.gov.sg</td></tr><tr><td>Production Environment</td><td>TBC</td><td>null</td><td></td></tr></tbody></table>

3. Go to the [form](https://go.gov.sg/sftp-interest-form).
4. Fill in the details.&#x20;
   * We will need your SSH keys. Refer to the following guide for instructions on generating ssh keys: [SSH Key Generation Guide](https://docs.oracle.com/en/cloud/cloud-at-customer/occ-get-started/generate-ssh-key-pair.html#GUID-8B9E7FCB-CEA3-4FB3-BF1A-FD3406A2432F)
   * Notification email: this is the email address from which you wish to receive results of the file upload.
5. Submit the form. Our team will add your account, then inform you.
6. Then [connect](https://guide-v2.postman.gov.sg/sftp/connecting-to-the-sftp-server) to our server, fill in the CSV file, and [drop](https://guide-v2.postman.gov.sg/sftp/sending-messages-via-sftp) it into our server

