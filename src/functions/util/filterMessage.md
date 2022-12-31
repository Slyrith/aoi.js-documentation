---
title: $filterMessage 
description: $filterMessage will filter certain characters.
id: filterMessage
---

`$filterMessage` will filter certain characters.

## Usage

```php
$filterMessage[text;...letters]
```

## Parameters 


| Field     | Type    | Description                                        | Required |
|-----------|---------|----------------------------------------------------|----------|
| text      | string  | text input which will be filtered                  | yes      |
| letters   | string  | characters you want to filter out of the `text`    | yes      |


## Example

This will remove the `N` of `Never` and return `ever`:

```javascript
bot.command({
  name: 'filterMessage',
  code: `
  $filterMessage[Never;N]
  `
});
```
