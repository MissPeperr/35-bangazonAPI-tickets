`Allow developers access to Customer resource -- TICKET 1`

> DONE
## Feature Criteria

Verbs to be supported

1. GET
2. POST
3. PUT
4. DELETE***

> ***This should be a **soft delete**. Meaning you should not actually delete the customer from the database. There is an `Active` flag on the customer table that should be set to false.

- User should be able to GET a list of customers, and GET a single customer. Results should not include **soft** deleted customers.
- If the query string parameter of `?include=products` is provided, then any products that the customer is selling should be included in the response.
- If the query string parameter of `q` is provided when querying the list of customers, then any customer that has a first or last name that matches the pattern should be returned.
> If `/customers?q=mic` is requested, then any customer whose first name is Michelle, or Michael, or Domicio should be returned. Any customer whose last name is Michaelangelo, or Omici, Dibromic should be returned.
