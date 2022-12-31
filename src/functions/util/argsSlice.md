---
title: $argsSlice 
description: $argsSlice will slice multiple arguments depending on the given text.
id: argsSlice
---

`$argsSlice` will slice multiple arguments depending on the given text.

## Usage

```php
$argsSlice[text;from?;to] 
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
  name: 'slice',
  code: `
  $argsSlice[Hello Bye;1;5]
  `
});
```
