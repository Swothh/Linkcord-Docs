# Gateway

> **Gateway URL** <br>
> You can view the instant presence of a user with the gateway
> ```
> wss://linkcord.js.org/api/wss?u={user_id}
> ```

## Payload

```json
{
    "op": 0, // number
    "d": {}, // data
    "t": "" // string
}
```

## Op Codes

| Code | Name          | Description                                             |
|------|---------------|---------------------------------------------------------|
| `0`  | `UPDATE_USER` | `Dispatched when user information or presence changes.` |
| `1`  | `FETCH_USER`  | `Dispatched when connected to the gateway.`             |

## Heartbeat

> The socket connection is pinged every 10 seconds, if the socket does <br> 
> not respond, the connection is terminated. (Socket answers automatically.)

## Example
```js
const ws = new WebSocket('wss://linkcord.js.org/api/wss?u=451444721089380373');

ws.onmessage = event => {
    try {
        const payload = JSON.parse(event.data);
        if (![ 0, 1 ].includes(payload.op)) return;
        if (![ 'FETCH_USER', 'UPDATE_USER' ].includes(payload.t)) return;
        console.log('user updated: 451444721089380373', payload.d);
    } catch {};
};

/*
user updated: 451444721089380373 {
  "op": 0,
  "t": "UPDATE_USER",
  "d": {
    "id": "451444721089380373",
    "username": "Swôth",
    "discriminator": "9990",
    "tag": "Swôth#9990",
    "avatar": "1cc37f9d16425b83a4a3b6e5559662fc",
    "avatar_url": "https://cdn.discordapp.com/avatars/451444721089380373/1cc37f9d16425b83a4a3b6e5559662fc.webp",
    "default_avatar": "https://cdn.discordapp.com/embed/avatars/0.png",
    "flags": 256,
    "status": "offline",
    "clients": {},
    "activities": []
  }
}
*/
```