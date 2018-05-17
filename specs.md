```
All bots are temporary.
If /start client doesn't log in for a month, deleted.
Normal human connections only do start once based on ip.
```


**GET** `/start`
```
UUID:  [\w]{,8}
TOKEN: [\w\D]{,8}

SERVERS []
```

**POST** `/connect form: uuid, token`
```
event logged_in

CLIENT_TOKEN
Websocket ID
```

# Websocket Events
**RECIEVE** `connected(shard)`
`connected(blob2)`

**SEND** `message(content)`

`message("Hello World!")`

**RECIEVE** `message(user, content)`

`message("AbCDe1234", "Hello World")`

**SEND** disconnect(type, reason)
**RECIEVE** disconnect(user, type, reason)
