# Errors

The Postman v2 API uses conventional HTTP response codes to indicate the success or failure of an API request. In general: Codes in the `2xx` range indicate success. Codes in the `4xx` range indicate a request that failed given the information provided (e.g., a required parameter was omitted, not having access to the campaign due to wrong API key, etc.). Codes in the `5xx` range indicate an error with Postman’s servers (these will be rare).

Some `4xx` errors that could be handled programmatically include an error code that briefly explains the error reported.



### Attributes

***

**message** string

A human-readable message providing more details about the error.

***

**statusCode** number

The HTTP status code of the error.

***

**HTTP status code summary**

<table><thead><tr><th width="266">Status code</th><th>What it means</th></tr></thead><tbody><tr><td>200 - OK</td><td>Everything worked as expected - you will get this status code for successful GET requests.</td></tr><tr><td>201 - Created</td><td>Everything worked as expected - your message(s) is/are created in our system. You will get this status code for successful POST requests that lead to the creation of messages.</td></tr><tr><td>400 - Bad Request</td><td>The request was unacceptable, often due to missing a required parameter.</td></tr><tr><td>401 - Unauthorized</td><td>No valid API key provided.</td></tr><tr><td>403 - Forbidden</td><td>The API key doesn't have permissions to perform the request.</td></tr><tr><td>404 - Not Found</td><td>The requested resource doesn't exist.</td></tr><tr><td>429 - Too Many Requests</td><td>Too many requests hit the API too quickly. We recommend an exponential backoff of your requests.</td></tr><tr><td>500, 502, 503, 504 - Server Errors</td><td>Something went wrong on Postman’s end. (These will be rare.)</td></tr></tbody></table>
