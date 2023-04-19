---
layout: default-layout
Title: Name - Dynamsoft Capture Vision Shared Parameters
Description: The parameter Name of Dynamsoft Capture Vision defines the unique identifier of top-level objects.
Keywords: top-level object, name, unique identifier
needAutoGenerateSidebar: true
noTitleIndex: true
permalink: /parameters/reference/shared-parameter/name.html
---

# Name

Represents the name of the top-level objects in Dynamsoft Capture Vision Parameter Template, which serves as its unique identifier.

## Example

```json
{
    "Name" : "cv_0"
}
```

## Parameter Summary

| Parameter Details |
| :----------------------------------- |
| **Type**<br>*String* |
| **Default Value**<br>It must be a mandatory setting value. |
| **Remarks**<br>It must be a unique name. |

**Note**: It is used as a unique identifier for the following top-level objects:

- [CaptureVisionTemplate Object](../../file/capture-vision-template.md)
- [ImageSource Object](../../file/image-source.md)
- [TargetROIDef Object](../../file/target-roi-definition/index.md)
- [SematicProcessing Object](../../file/semantic-processing/index.md)
- [BarcodeReaderTaskSetting Object](../../file/task-settings/barcode-reader-task-settings.md)
- [LabelRecognizerTaskSetting Object](../../file/task-settings/label-recognizer-task-settings.md)
- [DocumentNormalizerTaskSetting Object](../../file/task-settings/document-normalizer-task-settings.md)
- [CodeParserTaskSetting Object](../../file/task-settings/code-parser-task-settings.md)
- [ImageParameter Object](../../file/image-parameter.md)
- [BarcodeFormatSpecification Object](../../file/auxiliary/barcode-format-specification.md)
- [CharacterModel Object](../../file/auxiliary/character-model.md)
- [TextLineSpecification Object](../../file/auxiliary/textline-specification.md)
