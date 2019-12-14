`Allow developers to access the Order resource -- TICKET 4`

## Feature Criteria
Verbs to be supported

1. GET
2. POST
3. PUT
4. DELETE

- User should be able to GET a list, and GET a single item.
- When an order is deleted, every line item (i.e. entry in OrderProduct) should be removed
- Should be able to filter out completed orders with the `?completed=false` query string parameter. If the parameter value is true, then only completed order should be returned.
- If the query string parameter of `?_include=products` is in the URL, then the list of products in the order should be returned.
- If the query string parameter of `?_include=customers` is in the URL, then the customer representation should be included in the response.