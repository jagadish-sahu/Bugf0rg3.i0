* Hint : **What if Jeremy and Jessamy have the same token name?**  Lab variant: copypasta-`008`

  * Create two accounts and two tokens in `/api/tokens` with same token name 
  * In `/api/verify-token` use `X-API-Key : **TOKEN**` and verify both tokens created

* Hint : **Slugs are useful.**  Lab variant: copypasta-`009`

  * Create collection `POST` - `/api/collections` 
  * IDOR `/api/collections/2` admin and copy slug
  * Now share the created collection and paste the slug in link `/api/collections/share/xxslugxx`


* Hint : **Check your filters.**  Lab variant: copypasta-`011`

  * Create a test collection 
  * In private collection `/api/collections?filter%5Bvisibility%5D=private`
  * Change this to `/api/collections?filter[user_id][$ne]=private`

* Hint : **Try changing up your JSON when generating a token.**  Lab variant: copypasta-`013`

  * Create a snippet and create token `/api/tokens`
  * Use `X-API-Key` use documentation reader key to generate another token
  * Use this token for `X-API-Key` to `GET /api/snippets` and get flag
