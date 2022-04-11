# Widgets

## Spotify Large

#### Widget Code
```html
<iframe
    src="https://linkcord.js.org/api/v3/widget/{your_id}?type=spotify_large"
    width="600"
    height="150"
    allowtransparency="true"
    frameborder="0"
/>
```

#### Queries

| ?type= | `spotify_large` || ?language= | `en`, `de`, `tr` or `fr` || ?theme= | `light` or `dark` |
|--------|-----------------||------------|--------------------------||---------|-------------------|
| **?logo=** | **`true` or blank** || **?background=** | **`rgba` or `rgb`** |

> **Required Queries:** `?type=` <br>
> `?logo=` query removes `"Listening on Spotify"` text and adds a small logo.

#### Photos
![light](https://cdn.discordapp.com/attachments/963127332095266826/963131131547496498/unknown.png)
![dark](https://cdn.discordapp.com/attachments/963127332095266826/963131285075812362/unknown.png)

---

## Spotify Small

#### Widget Code
```html
<iframe
    src="https://linkcord.js.org/api/v3/widget/{your_id}?type=spotify_small"
    width="150"
    height="150"
    allowtransparency="true"
    frameborder="0"
/>
```

#### Queries

| ?type= | `spotify_small` || **?background=** | **`rgba` or `rgb`** || ?theme= | `light` or `dark` |
|--------|-----------------||------------------|---------------------||---------|-------------------|

> **Required Queries:** `?type=`

#### Photos
![light](https://cdn.discordapp.com/attachments/963127332095266826/963131619412148245/unknown.png)
![dark](https://cdn.discordapp.com/attachments/963127332095266826/963131508816752640/unknown.png)

---

## Visual Studio Code

#### Widget Code
```html
<iframe
    src="https://linkcord.js.org/api/v3/widget/{your_id}?type=vsc"
    width="600"
    height="150"
    allowtransparency="true"
    frameborder="0"
/>
```

#### Queries

| ?type= | `vsc` || ?language= | `en`, `de`, `tr` or `fr` || ?theme= | `light` or `dark` |
|--------|-----------------||------------|--------------------------||---------|-------------------|
| **?background=** | **`rgba` or `rgb`** |

> **Required Queries:** `?type=` <br>
> `!!! Important: This widget only works with the "Discord Presence" plugin.` <br>
> **[Click to view the plugin!](https://marketplace.visualstudio.com/items?itemName=icrawl.discord-vscode)**

#### Photos
![light](https://cdn.discordapp.com/attachments/963127332095266826/963131821548249158/unknown.png)
![dark](https://cdn.discordapp.com/attachments/963127332095266826/963131931254485002/unknown.png)

---

## Custom Status

#### Widget Code
```html
<iframe
    src="https://linkcord.js.org/api/v3/widget/{your_id}?type=status"
    width="300"
    height="100"
    allowtransparency="true"
    frameborder="0"
/>
```

#### Queries

| ?type= | `status` || ?size= | `a number` or `full` || ?theme= | `light` or `dark` |
|--------|-----------------||------------|--------------------------||---------|-------------------|
| **?background=** | **`rgba` or `rgb`** |

> **Required Queries:** `?type=`

#### Photos
![light](https://cdn.discordapp.com/attachments/963127332095266826/963132108040192020/unknown.png)
![dark](https://cdn.discordapp.com/attachments/963127332095266826/963132194216362044/unknown.png)