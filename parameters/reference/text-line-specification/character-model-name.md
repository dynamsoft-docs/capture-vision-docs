---
layout: default-layout
title: CharacterModelName - Dynamsoft Label Recognizer Parameters
description: The parameter CharacterModelName of Dynamsoft Label Recognizer defines the name of character models.
keywords: Character model
---

# CharacterModelName

The `CharacterModelName` parameter references the character model by its name.

## JSON Structure

**Location in template:**
```
TextLineSpecificationOptions[i]
    └── CharacterModelName
```

**Parent object:** [TextLineSpecification]({{ site.dcvb_parameters }}file/auxiliary/text-line-specification.html) object

**Example:**

```json
{
    "CharacterModelName": "NumberLetterCharRecognition"
}
```

> [!NOTE]
> - This snippet shows only the `CharacterModelName` parameter.
> - To use it, embed this parameter within a [TextLineSpecification]({{ site.dcvb_parameters }}file/auxiliary/text-line-specification.html) object.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)


## Parameter Details

| CharacterModelName Parameter Details |
| :----------------------------------- |
| **Type**<br>*String* |
| **Range**<br>The name of a Character Model object that defined in `CaptureVisionModelOptions`. |
| **Default Value**<br>"NumberLetterCharRecognition" |
