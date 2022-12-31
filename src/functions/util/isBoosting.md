---
title: $isBoosting 
description: $isBoosting will slide multiple arguments depending on the arguments.
id: isBoosting
---

`$isBoosting` will slide multiple arguments depending on the arguments.

## Usage

```php
$isBoosting[text;from;to?]
```

## Parameters 


| Field     | Type    | Description                                        | Required |
|-----------|---------|----------------------------------------------------|----------|
| text      | string  | text you want to slice                             | yes      |
| from?     | number  | starting point where to slice the message          | no       |
| to        | number  | ending point where slicing ends                    | yes      |


## Example

This will return `Bye` and remove `Hello` from the given text:

```javascript
bot.command({
  name: 'isBoosting',
  code: `
  $isBoosting[Hello Bye;1;5]
  `
});
```
