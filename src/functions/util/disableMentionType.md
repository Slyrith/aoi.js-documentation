---
title: $disableMentionType 
description: $disableMentionType will disable a specific mention type.
id: disableMentionType
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
<@$authorID>
$disableMentionType[users] 
  `
});
```

This will stop the bot from mentioning anyone or anything:

```javascript
bot.command({
  name: 'mention',
  code: `
<@$authorID>
$disableMentionType[all] 
  `
});
```
