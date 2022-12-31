---
title: $fetch 
description: $fetch will fetch information about a given method using Discord API.
id: fetch
---

`$fetch` will fetch information about a given method using Discord API.

## Usage

```php
$fetch[method;query;...query]
```
### Methods

| Method     | Example    | Description                                        | Required |
|------------|---------|----------------------------------------------------|----------|
| message       | `$fetch[message;$messageID]` | text you want to slice                             | yes      |
| channel      | `$fetch[channel;$channelID]`  | starting point where to slice the message          | no       |
| user         | `$fetch[user;$authorID]`  | ending point where slicing ends                    | yes      |
| invite         | `$fetch[invite;https://discord.gg/aoi-js-server-akarui-development-team-773352845738115102]`  | ending point where slicing ends                    | yes      |
| webhook         | `$fetch[webhook geID]`  | ending point where slicing ends                    | yes      |
| application         | `$fetch[message;$messageID]`  | ending point where slicing ends                    | yes      |
| command         | `$fetch[message;$messageID]`  | ending point where slicing ends                    | yes      |
| guildPreview         | `$fetch[message;$messageID]`  | ending point where slicing ends                    | yes      |
| guildTemplate         | `$fetch[message;$messageID]`  | ending point where slicing ends                    | yes      |
| premiumStickerPacks         | `$fetch[message;$messageID]`  | ending point where slicing ends                    | yes      |
| sticker         | `$fetch[message;$messageID]`  | ending point where slicing ends                    | yes      |
| guildCommand         | `$fetch[message;$messageID]`  | ending point where slicing ends                    | yes      |
| default         | `$fetch[message;$messageID]`  | ending point where slicing ends                    | yes      |

## Parameters 


| Field     | Type    | Description                                        | Required |
|-----------|---------|----------------------------------------------------|----------|
| text      | string  | text you want to slice                             | yes      |
| from?     | number  | starting point where to slice the message          | no       |
| to        | number  | ending point where slicing ends                    | yes      |


## Example

This will return `Bye` and remove `Hello` from the given text:

```javascript
bot.command({
  name: 'slice',
  code: `
  $argsSlice[Hello Bye;1;5]
  `
});
```
