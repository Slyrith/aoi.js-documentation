---
title: $emojisFromMessage 
description: $emojisFromMessage will retrieve all emojis given in a message.
id: emojisFromMessage
---

`$emojisFromMessage` returns all emojis in a given message.

## Usage

```php
$emojisFromMessage
```

## Example

This will return any emojis you give as argument:

```javascript
bot.command({
  name: 'emojisFromMessage',
  code: `
$emojisFromMessage
  `
});
```
