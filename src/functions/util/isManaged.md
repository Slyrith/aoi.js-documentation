---
title: $isManaged 
description: $isManaged will check if a certain role is managed by Discord.
id: isManaged
---

`$isManaged` will check if a certain role is managed by Discord.

## Usage

```php
$isManaged[roleID;guildID?]
```

## Parameters 


| Field     | Type    | Description                                        | Required |
|-----------|---------|----------------------------------------------------|----------|
| roleID      | integer  | role ID of the role you want to check if it's managed by Discord or not        | yes      |
| guildID?     | integer  | guild ID of where the role exists          | no       |

### Please note that your bot has to be in the same server as the role or else this function will not work.

## Example

This will check if a role called `Server Booster` is managed by Discord.

```javascript
bot.command({
  name: 'isManaged',
  code: `
  $isManaged[$findRole[Server Booster];$guildID]
  `
});
```
