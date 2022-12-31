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
| type      | string  | type of mention you want to disable                | yes      |

### Available types
* everyone
  * disables everyone/here mentions
* users
  * disables all user mentions
* roles
  * disables all role mentions
* all
  * disables all mentions stated above  
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
