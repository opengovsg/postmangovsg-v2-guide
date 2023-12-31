# Authentication

The Postman v2 API uses [API keys](../postman-v2-admin-portal/campaign-settings.md#api-keys) and static [IP whitelisting](../postman-v2-admin-portal/campaign-settings.md#ip-address-whitelisting) to authenticate incoming requests from your server.

Your API keys carry many privileges, so be sure to keep them secure. Don't share your secret API keys in publicly accessible areas such as GitHub, client-side code, and so forth.

Authentication to the API is performed with [HTTP Bearer Auth](https://developer.mozilla.org/en-US/docs/Web/HTTP/Authentication#authentication\_schemes).&#x20;

{% hint style="info" %}
You will first need to [Create Campaign](../postman-v2-admin-portal/create-campaign.md) before you can generate your `campaignId`
{% endhint %}

{% code title="An example curl request:" overflow="wrap" %}
```sh
curl https://<POSTMAN_V2_API_BASE_URL>/api/v2/campaigns/:campaignId/messages -H "Authorization: Bearer YOUR_API_KEY"
```
{% endcode %}

You must make all API calls over [HTTPS](http://en.wikipedia.org/wiki/HTTP\_Secure). Calls that you make over plain HTTP will fail. API requests without authentication will also fail.

If you make a request without authentication, you will receive HTTP 401 and the following in your response body:

```json
{
    "message": "Unauthorized",
    "statusCode": 401
}
```
