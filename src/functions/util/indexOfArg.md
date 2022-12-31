---
title: $indexOfArg
description: $indexOfArg will return the index of the given query.
id: indexOfArg
---

<!-- not finished, missing example and correct usage -->
<!-- not finished, missing example and correct usage -->
<!-- not finished, missing example and correct usage -->
<!-- not finished, missing example and correct usage -->


`$indexOfArg` will return the index of the given query.

## Usage

```php
$indexOfArg[string;query]
```

## Parameters 


| Field     | Type    | Description                                        | Required |
|-----------|---------|----------------------------------------------------|----------|
| string    | string  | the text the bot will be checking the index of                            | yes      |
| query     | string  | the query the bot will be checking for          | yes      |


## Example

???

```javascript
bot.command({
  name: 'indexOfArgs',
  code: `
  $indexOfArgs[..]
  `
});
```
