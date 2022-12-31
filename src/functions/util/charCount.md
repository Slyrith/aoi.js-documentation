---
title: $charCount 
description: $charCount will count the given arguments.
id: charCount
---

`$charCount` will count the given text and return the amount of characters.

## Usage

```php
$charCount[text]
```

## Parameters 


| Field     | Type    | Description                                        | Required |
|-----------|---------|----------------------------------------------------|----------|
| text      | string  | arguments where you count the character            | yes      |


## Example

This will return `77` as there are 77 characters in this text:

```javascript
bot.command({
  name: 'charCount',
  code: `
  $charCount[aoi.js is one of the simplest and easiest ways to create your own Discord Bot]
  `
});
```
