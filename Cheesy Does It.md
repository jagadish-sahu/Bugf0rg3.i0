* Hint : **Can apply the discount multiple times?**

  * Given discount code `PIZZA-10`
  * Place a order with discount code `/api/orders`;
```text
"discount":["PIZZA-10","PIZZA-10"]
```


* Hint : **My favourite bug is mass assignment.**

  * Place an order, look at `GET https://[link]/api/orders/1`
  * Change it to `PATCH https://[link]/api/orders/2`
  * And add ```Content-Type : application/json```
  * Place another order and send the changes immediately;
