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
## Parameters 


| Field     | Type    | Description                                        | Required |
|-----------|---------|----------------------------------------------------|----------|
| method    | string  | method (listed below)                              | yes      |
| query     | string  | input for the method                               | yes      |

### Methods

| Method     | Example    | Description                                        
|------------|---------|----------------------------------------------------|
| message       | `$fetch[message;$messageID]` | Retrieve information about a message                             |
| channel      | `$fetch[channel;$channelID]`  | Retrieve information about a channel         |
| user         | `$fetch[user;$authorID]`  | Retrieve information about an user                    |
| invite         | `$fetch[invite;https://discord.gg/aoi-js-server-akarui-development-team-773352845738115102]`  | Retrieve information about an invite|
| webhook         | `$fetch[webhook;webhookID]`  | Retrieve information about a webhook                    |
| application         | `$fetch[application;$clientID]`  | Retrieve information about an application                    |
| command         | `$fetch[command;application command ID]`  | Retrieve information about an application command                    |
| guildPreview         | `$fetch[guildPreview;???]`  | Retrieve information about a guild preview                    |
| guildTemplate         | `$fetch[guildTemplate;template ID]`  | Retrieve information about a guild template                    |
| premiumStickerPacks         | `$fetch[premiumStickerPacks;$messageID]`  | ???                    |
| sticker         | `$fetch[sticket;sticker ID]`  | Retrieve information about a sticker                     |
| guildCommand         | `$fetch[guildCommand;???]`  | ???                    |
| default         | `$fetch[message;option ID]`  | ???                    |


## Example

This will display information about the message which execute the `fetch` command:

```javascript
bot.command({
  name: 'fetch',
  code: `
  \`\`\`
  $fetch[message;$messageID]
  \`\`\`
  ` 
});
```
