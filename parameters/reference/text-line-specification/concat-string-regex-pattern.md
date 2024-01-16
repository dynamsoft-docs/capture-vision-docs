---
layout: default-layout
title: ConcatStringRegExPattern - Dynamsoft Label Recognizer Parameters
description: The parameter ConcatStringRegExPattern of text line specification is for specifying the regex pattern of the concated text lines.
keywords: concat string regex pattern, parameter reference, parameter
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---

# ConcatStringRegExPattern

Specifies the regular expression pattern of the concated text lines. It is used to correct the recognized line text.

## Example

```json
{
    "ConcatStringRegExPattern":""
}
```

## Parameter Summary

| Parameter Details |
| :----------------------------------- |
| **Type**<br>*String* |
| **Range**<br>The supported regular expression pattern syntax is shown in the following table.|
| **Default Value**<br>"" |
| **Remarks**<br>It is used to correct the recognized line text. |

Supported regular expressions pattern syntax:

| characters | matches |
| ---------- | ------- |
| \d         | a decimal digit character (same as "[0-9]"). |
| \D         | any character that is not a decimal digit character (same as "[^0-9]"). |
| \s         | a whitespace character (same as " " or "[ ]"). |
| \S         | any character that is not a whitespace character (same as "[^ ]"). |
| \w         | an alphanumeric or underscore character (same as "[0-9A-z_]"). |
| \W         | any character that is not an alphanumeric or underscore character (same as "[^0-9A-z_]"). |
| [class]    | any character that is part of the class. |
| [^class]   | any character that is not part of the class. |
| *          | The preceding atom is matched 0 or more times. |
| +          | The preceding atom is matched 1 or more times. |
| ?          | The preceding atom is optional (matched either 0 times or once). |
| (subpattern) | Groups a sequence of subpatterns as a matching atom. |
| {`n`}        | The preceding atom is matched exactly `n` times. |
| {`min`,}     | The preceding atom is matched `min` or more times. |
| {,`max`}     | The preceding atom is matched at least 0 times, but not more than `max`. |
| {`min`,`max`}  | The preceding atom is matched at least `min` times, but not more than `max`. |
| {(`n`)}       | The preceding atom matches exactly `n` characters. |
| {(`min`,)}    | The preceding atom matches `min` or more characters. |
| {(,`max`)}    | The preceding atom matches at least 0 characters, but not more than `max`. |
| {(`min`,`max`)} | The preceding atom matches at least `min` characters, but not more than `max`. |
| [(`string1`,`string2`,...)] | any case insensitive string that is one of the listed strings separated by commas (,). For example: [(CAN,USA)] matches CAN, USA or can. |
| [(`minnumericstring`-`maxnumericstring`)] | a numeric string that is between `minnumericstring` and `maxnumericstring`. For example: [(01-12)] matches 01, 02, 03, ... until 12). |
