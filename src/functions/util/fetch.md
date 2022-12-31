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
| message       | `$fetch[message;$messageID]` | Retrieve information about a message                             | yes      |
| channel      | `$fetch[channel;$channelID]`  | Retrieve information about a channel         | no       |
| user         | `$fetch[user;$authorID]`  | Retrieve information about an user                    | yes      |
| invite         | `$fetch[invite;https://discord.gg/aoi-js-server-akarui-development-team-773352845738115102]`  | Retrieve information about an invite                    | yes      |
| webhook         | `$fetch[webhook;webhookID]`  | Retrieve information about a webhook                    | yes      |
| application         | `$fetch[application;$clientID]`  | Retrieve information about an application                    | yes      |
| command         | `$fetch[command;application command ID]`  | Retrieve information about an application command                    | yes      |
| guildPreview         | `$fetch[guildPreview;???]`  | Retrieve information about a guild preview                    | yes      |
| guildTemplate         | `$fetch[guildTemplate;template ID]`  | Retrieve information about a guild template                    | yes      |
| premiumStickerPacks         | `$fetch[premiumStickerPacks;$messageID]`  | ???                    | yes      |
| sticker         | `$fetch[sticket;sticker ID]`  | Retrieve information about a sticker                     | yes      |
| guildCommand         | `$fetch[guildCommand;???]`  | ???                    | yes      |
| default         | `$fetch[message;option ID]`  | ???                    | yes      |

## Parameters 


| Field     | Type    | Description                                        | Required |
|-----------|---------|----------------------------------------------------|----------|
| method    | string  | method (listed below)                              | yes      |
| query      string  | starting point where to slice the message          | yes      |


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
