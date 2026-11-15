* Hint : **Make sure you leave some delivery instructions.** - Lab variant: `cafeclub-011`

  * In checkout `/api/checkout`
  * delivery_instructions: `{{.}}`
  * Preview invoice


* Hint : **Can you checkout with more items than you initially added to your basket?** - Lab variant: `cafeclub-005`

  * Use `Burp suite` complete one order 
  * Move post requests from proxy history to repeater `/api/cart` and `/api/checkout`
  * In repeater duplicate `/api/cart` 5 times and group all requests including `/api/checkout` 
  * In all `/api/cart` requests change "product_id"
  * Send the group in parallel and get flag in `/api/checkout`
