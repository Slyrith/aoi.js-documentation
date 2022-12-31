---
title: $argsSlice 
description: $argsSlice will slide multiple arguments depending on the arguments.
id: argsCheck
---

`$argsSlice` will slide multiple arguments depending on the arguments.

## Usage

```php
$argsSlice[text;from;to?]
```

## Parameters 


| Field         | Type    | Description                                                | Required |
|---------------|---------|------------------------------------------------------------|----------|
| text          | string  | text you want to slice                                     | yes      |
| from sing  | error message when invalid mathematical notation are used  | no       |

## Example

This will return `false` as 240 is greater than 200:

```javascript
bot.command({
  name: 'checkCondition',
  code: `
  $checkCondition[200>240]
  `
});
```
