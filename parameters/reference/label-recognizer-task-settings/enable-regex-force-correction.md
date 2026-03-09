---
layout: default-layout
title: EnableRegexForceCorrection - Dynamsoft Label Recognizer Parameters
description: Reference for the EnableRegexForceCorrection parameter in the Dynamsoft Capture Vision LabelRecognizerTaskSetting, which controls whether the SDK forcibly corrects recognized text to match the configured regular expression pattern (1 = force correction enabled, 0 = disabled).
keywords: text lines, concatenated strings, regular expression
---

# EnableRegexForceCorrection

Parameter `EnableRegexForceCorrection` specifies whether to enable forced correction based on the regular expression pattern.

## JSON Structure

**Location in template:**

```
LabelRecognizerTaskSettingOptions[i]
    └── SectionArray[j] (Section object)
        └── StageArray[k] (Stage object where Stage = "SST_RECOGNIZE_RAW_TEXT_LINES")
            └── EnableRegexForceCorrection
```

**Parent object:** [RecognizeRawTextLinesStage]({{ site.dcvb_parameters }}reference/label-recognizer-task-settings/stage-recognize-raw-text-lines.html)

**Example:**

```json
{
    "EnableRegexForceCorrection": 1
}
```

> [!NOTE]
> - This snippet shows only the `EnableRegexForceCorrection` parameter.
> - To use it, embed this parameter within a [RecognizeRawTextLinesStage]({{ site.dcvb_parameters }}reference/label-recognizer-task-settings/stage-recognize-raw-text-lines.html) object.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json)

## Parameter Details

| EnableRegexForceCorrection Parameter Details |
| :----------------------------------- |
| **Type**<br>*int* |
| **Range**<br>0, 1|
| **Default Value**<br>1 |
