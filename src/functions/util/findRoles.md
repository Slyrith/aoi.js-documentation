---
title: $findRoles 
description: $findRoles will return roles depending on the given query.
id: findRoles
---

`$findRoles` will return roles depending on the given query.

## Usage

```php
$findRoles[query;limit?;type?;res?]
```

## Parameters 


| Field     | Type    | Description                                        | Required |
|-----------|---------|----------------------------------------------------|----------|
| query      | string  |  name of the role you want to find                            | yes      |
| limit?     | number  |  the maximum amount of roles the bot will return         | no       |
| type?        | string  |     ..             | no      |
| res?        | string  |     ..                | no      |


## Example

This will return all roles which are named `Owner`:

```javascript
bot.command({
  name: 'findRoles',
  code: `
  $findRoles[Owner;5;startsWith;{position}) {username}: {id}]
  `
});
```
