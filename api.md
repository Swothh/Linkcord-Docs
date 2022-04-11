# API

## GraphQL

> Check out the playground to test GraphQL and view its documentation. <br>
> https://linkcord.js.org/api/graphql

### QUERY - user(id: String!)
```graphql
query {
    user(id: String!) {
        id: String!
        username: String!
        discriminator: String!
        tag: String!
        avatar: String
        avatar_url: String
        default_avatar: String
        flags: Int!
        status: String!
        clients: {
            desktop: String
            mobile: String
            web: String
        }!
        activities: [{
            name: String!
            type: String!
            details: String
            state: String
            emoji: {
                id: String
                name: String
            }
            app_id: String
            timestamps: {
                start: Int
                end: Int
            }
            assets: {
                large_text: String
                small_text: String
            }
            url: {
                large_image: String
                small_image: String
            }
        }]!
    }
}
```

## REST

### GET - /api/v3/user/:id

```
https://linkcord.js.org/api/v3/user/:id
```

##### Params

| *Name*   | *Required*   | *Description*     |
|----------|--------------|-------------------|
| `id`     | `true`       | `Discord User ID` |

##### Queries

| *Name*   | *Required*   | *Description*     |
|----------|--------------|-------------------|
| `-`      | `-`          | `-`               |

##### Response
```json
{
  "data": {
    "id": "915326086932484126",
    "username": "berk",
    "discriminator": "5208",
    "tag": "berk#5208",
    "avatar": "e9027e4bea8dd32a63dab09c0846cf26",
    "avatar_url": "https://cdn.discordapp.com/avatars/915326086932484126/e9027e4bea8dd32a63dab09c0846cf26.webp",
    "default_avatar": "https://cdn.discordapp.com/embed/avatars/3.png",
    "flags": 256,
    "status": "offline",
    "clients": {
      
    },
    "activities": [
      
    ]
  }
}
```

---

### GET - /api/v3/widget/:id

```
https://linkcord.js.org/api/v3/widget/:id
```

##### Params

| *Name*   | *Required*   | *Description*     |
|----------|--------------|-------------------|
| `id`     | `true`       | `Discord User ID` |

##### Queries

| *Name*   | *Required*   | *Description*     |
|----------|--------------|-------------------|
| `-`      | `-`          | `-`               |

##### Response
```json
Returns a resizable widget.
```