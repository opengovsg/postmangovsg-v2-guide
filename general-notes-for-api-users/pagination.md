# Pagination

We are using a Cursor-based pagination, a method of pagination that uses a unique identifier (cursor) to keep track of the current position in the dataset.

Here's a general overview of how it works:

1. **Usage**: The [Retrieve Batch API](../endpoints-for-api-users/retrieve-batch.md) takes in parameters such as `limit`, `search` ,`before`, and `after` to control the pagination.
2. **Cursor**: The `before` and `after` parameters are used to specify the cursor for fetching the previous or next page of results. The cursor typically represents the position of a specific record in the dataset.
3. **Sorting**: The data is sorted by the `createdAt` followed by `id`
4. **Result**: The response returns the paginated results along with cursors for the next and previous pages, allowing for easy navigation through the dataset.

{% code title="Example Response" %}
```
{
  "data": [
    {
      "id": "message_62a2a141-97f8-4fc8-82db-36f539228322",
      "recipient": "6599999999",
      "values": {
        "recipientName": "Emily Yeo",
        "topic": "passport application #12345F"
      },
      "language": "english",
      "latestStatus": "success",
      "error": ""
    },
    ...
  ],
  "pageData": {
		"hasNextPage": false,
		"hasPreviousPage": false,
		"startCursor": "WyIyMDIzLTEwLTI0VDE3OjQwOjI1Ljk2OCswODowMCIsIm1lc3NhZ2VfM2E1MWI1ODctMzQ5OS00YTBmLTlkNGUtZTRlOWYzNWZkNmMxIl0=",
		"endCursor": "WyIyMDIzLTEwLTI0VDE3OjQwOjI1Ljk2OCswODowMCIsIm1lc3NhZ2VfM2E1MWI1ODctMzQ5OS00YTBmLTlkNGUtZTRlOWYzNWZkNmMxIl0="
	}
}
```
{% endcode %}

For example:

1. `hasNextPage` tells you if there's a next page in the queried `data` object
   1. To go to the next page, you can use the `after` Query Parameter with the current page's `endCursor` value.
2. `hasPreviousPage`tells you if there's a previous page in the queried `data` object
   1. To go to the previous page, you can use the `before` Query Parameter with the current page's `startCursor` value.



List of Apis that has pagination

1. [Retrieve Batch](../endpoints-for-api-users/retrieve-batch.md)
