---
layout: default-layout
title: CharSet - CharacterModel - Dynamsoft Capture Vision Parameters
description: The parameter CharSet defines a path of character models.
keywords: Directory path
needAutoGenerateSidebar: true
noTitleIndex: true
needGenerateH3Content: true
---

# CharSet

Parameter `CharSet` is an object that defines specific configurations for character recognition. It allows for the inclusion of special characters and the exclusion of certain characters, providing more control over which characters are recognized or ignored during processing.

## Example

```json
{
    "CharSet": {
        "AddSpecialChars": ["-", ":"],
        "ExcludeChars": ["O", "Q"]
    }
}
```

## Parameter Summary

### Arguments

<table style = "text-align:left">
    <thead>
        <tr>
            <th nowrap="nowrap">Argument Name</th>
            <th nowrap="nowrap">Argument Summary</th>
        </tr>
    </thead>
    <tr>
        <td rowspan = "4" style="vertical-align:text-top">AddSpecialChars<br>(Required)</td>
        <td><b>Description</b><br>It is an array that specifies additional special characters to be recognized.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>string array</i>
        </td>
    </tr>
    <tr>
        <td><b>Range</b><br>hyphen (-)
            <br>underscore (_)
            <br>colon (:)
            <br>space ( )
            <br>period (.)
        </td>
    </tr>
	<tr>
        <td><b>Default Value</b><br>null</b>: It means no extra special characters are recognized unless explicitly added.
        </td>
    </tr>
    <tr>
        <td rowspan = "4" style="vertical-align:text-top">ExcludeChars<br>(Optional)</td>
        <td><b>Description</b><br>It is an array that specifies characters to be excluded from recognition.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>string array</i>
        </td>
    </tr>
    <tr>
        <td><b>Range</b><br>It is dependent on the character model: <br>
		Number: [0-9] <br>
		Letter: [a-zA-Z] <br>
		UpperCase: [A-Z] <br>
		LowerCase: [a-z] <br>
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br><b>null</b>: It means no characters are excluded unless explicitly specified.
        </td>
    </tr>
</table>
