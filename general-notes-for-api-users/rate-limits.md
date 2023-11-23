# Rate Limits

The Postman v2 API uses a number of safeguards against bursts of incoming traffic to help maximise its stability. If you send many requests in quick succession, you might see error responses that show up as status code `429`.

Note that we **do not** queue requests which arrive past the rate limit and such requests are dropped. As such, you will need to retry the same request(s) later.
