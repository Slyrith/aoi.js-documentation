---
title: $function
description: Short description of the function.
id: function-name
---

## Usage

```php
$function[param1;param2]
```

## Parameters 

> *If there is even one parameter, it should be used.*

| Field  | Type    | Description     | Required |
|--------|---------|-----------------|----------|
| param1 | string  | it shows param1 | yes      |
| param2 | integer | it shows param2 | no       |

### Parameter Types
> *Required if the parameter has other options*

* `a` — A type
* `b` — B type

## Example(s)

This returns: ...

```javascript
bot.command({
  name: 'function-name',
  code: `
  $function[index;aoijs]
  `
});
```