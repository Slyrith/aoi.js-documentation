---
title: $findNumbers 
description: $findNumbers will attempt to retrieve all numbers in a message and return those.
id: findNumbers
---

`$findNumbers` will attempt to retrieve all numbers in a message and return those.

## Usage

```php
$findNumbers[text]
```

## Parameters 


| Field     | Type    | Description                                        | Required |
|-----------|---------|----------------------------------------------------|----------|
| text      | string  | text where you want to find numbers                             | yes      |


## Example

This will return `25` and remove `Hello, I'm [..] years old` from the given text:

```javascript
bot.command({
  name: 'findNumbers',
  code: `
  $findNumbers[Hello, I'm 25 years old]
  `
});
```
