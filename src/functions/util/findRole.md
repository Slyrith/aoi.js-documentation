---
title: $findRole 
description: $findRole will search and return a given role of a certain guild.
id: findRole
---

`$findRole` will search and return a given role of a certain guild.

## Usage

```php
$findRole[roleResolver;guildID?]
```

## Parameters 


| Field     | Type    | Description                                        | Required |
|-----------|---------|----------------------------------------------------|----------|
| roleResolver      | string  | text you want to slice                             | yes      |
| guildID?     | integer  | guild ID where the role is present in          | no       |


## Example

This will return `773353338393329675`:
### Note that this won't work if your bot is not in the guild where the role is in.
```javascript
bot.command({
  name: 'findRole',
  code: `
  $findRole[Owner;773352845738115102]
  `
});
```
