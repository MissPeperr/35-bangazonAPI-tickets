`Allow developers to access Product resource -- TICKET 2`

> DONE
## Feature Criteria
Verbs to be supported

1. GET
2. POST
3. PUT
4. DELETE

- User should be able to GET a list of products, and GET a single product by Id.
- If the query string parameter `?sortBy=recent` is provided in the URL when querying a list of products, then all of the products that were most recently created should appear first.
- If the query string parameter `q` is provided in the URL when querying a list of products, then all of the products whose title or description includes the search parameter should be returned.
> If the query string parameter `?q=tank` is provided in the URL when querying a list of products, then all of the products whose title or description contains the word tank should be returned.