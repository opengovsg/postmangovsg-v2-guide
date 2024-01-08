# 🗒 Overview

The Postman v2 API is organised around REST. Our API has predictable resource-oriented URLs, accepts JSON request bodies, returns JSON response bodies, and uses standard HTTP response codes, authentication, and verbs.

To optimise performance and reliability, Postman v2 has established rate limits and allocations for API endpoints ([Rate limits](rate-limits.md)).

{% code title="Base Url" %}
```
https://<POSTMAN_V2_API_BASE_URL>/api/v2
```
{% endcode %}

#### Test Environment Base URL

<table><thead><tr><th width="196">Type</th><th width="267">Base URL</th><th>Remarks</th></tr></thead><tbody><tr><td>Postman API </td><td><a href="https://test.sgc.gov.sg/api/v2">https://test.sgc.gov.sg</a></td><td></td></tr><tr><td>Postman Admin Portal</td><td><a href="https://test.sgc.gov.sg/api/v2">https://test.sgc.gov.sg</a></td><td></td></tr></tbody></table>

#### Production Environment Base URL

| Type                            | Base URL |                            |
| ------------------------------- | -------- | -------------------------- |
| Postman API Production Platform |          | To be released in May 2024 |
| Postman Admin Platform          |          | To be released in May 2024 |
