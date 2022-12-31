---
title: $disableMentionType 
description: $disableMentionType will disable a specific mention type.
id: argsCheck
---

`$disableMentionType` will disable a specific mention type.

## Usage

```php
$disableMentionType[type]
```

## Parameters 


| Field     | Type    | Description                                        | Required |
|-----------|---------|----------------------------------------------------|----------|
| type      | string  | "everyone", "users", "roles", "all"                | yes      |


## Example(s)

This will stop the bot from mentioning you:

```javascript
bot.command({
  name: 'mention',
  code: `
$disableMentionType[users] 
<@$authorID>
  `
});
```

This will stop the bot from mentioning anyone or anything:

```javascript
bot.command({
  name: 'mention',
  code: `
$disableMentionType[all] 
<@$authorID>
  `
});
```
