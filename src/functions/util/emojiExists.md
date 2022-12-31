---
title: $emojiExists 
description: $emojiExists will check if the given emoji exists.
id: argsCheck
---

`$emojiExists` will check if the given emoji exists.

## Usage

```php
$emojiExists[emoji]
```

## Parameters 


| Field     | Type    | Description                                        | Required |
|-----------|---------|----------------------------------------------------|----------|
| emoji     | string  | emoji you want to check if it exists               | yes      |

### Please note that your bot has to be present in the guild where the emoji is in.

## Example

This will return `true` as the <img src="https://cdn.discordapp.com/emojis/1003365344724910191.webp?size=96&quality=lossless" width="19"> emoji exists:

```javascript
bot.command({
  name: 'emojiExists',
  code: `
  $emojiExists[<:LerefMoney:1003365344724910191>]
  `
});
```
