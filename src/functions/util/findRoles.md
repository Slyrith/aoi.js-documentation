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
| query      | string  |                              | yes      |
| limit?     | number  |           | no       |
| type?        | string  |                  | no      |
| res?        | string  |                     | no      |


## Example

This will return `Bye` and remove `Hello` from the given text:

```javascript
bot.command({
  name: 'slice',
  code: `
  $findRoles[query;limit?;type?;res?]
  `
});
```
