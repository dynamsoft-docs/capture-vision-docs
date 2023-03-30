---   
layout: default-layout
title:  CharacterModel - Dynamsoft Capture Vision Parameter File
description: The CharacterModel object in the Dynamsoft Capture Vision Parameter File defines how the charactor models are found.
keywords: Text line specification
needAutoGenerateSidebar: true
noTitleIndex: true
---

# CharacterModel

Character models are required when implementing text line recognition.
`CharacterModel` objects are defined under `CharacterModelOptions`.

```json
{
    "Name": "NumberLetter",
    "DirectoryPath" : "D:\\CharacterModel\\",
    "FilterFilePath" : "D:\\exclude.txt"
}
```

`CharacterModels` are the models that specially trained for character recognizing.

<div align="center">
   <p><img src="../assets/character-model.png" alt="character-model" width="20%" /></p>
   <p>Example of CharacterModel files</p>
</div>

In the CharacterModel files consist of

- Model files (Required):
- Assist model files (Optional):
- Filter files (Optional): Set which characters are included or excluded from the text line recognition.

## How to Use Filter File

Example of a exclude filter file.

```txt
exclude
I Q O
```

You can define the filter file in the same folder with the model files. For example:

```json
{
    "Name" : "NumberUppercase",
    "DirectoryPath" : "D:\\CharacterModel\\",
    "FilterFilePath" : "D:\\CharacterModel\\Exclude.txt"
}
```

You can define a same filter file for different `CharacterModel` objects.

```json
{
    "Name" : "VINModel",
    "DirectoryPath" : "D:\\VIN\\",
    "FilterFilePath" : "D:\\VIN\\Exclude.txt"
},
{
    "Name" : "MRZModel",
    "DirectoryPath" : "D:\\MRZ\\",
    "FilterFilePath" : "D:\\VIN\\Exclude.txt"
}
```

## As a Parameter of TextLineSpecification Object

You can specify a `CharacterModel` name for your `TextLineSpecification` parameter mode.

```json
{
    "Name":"",
    "CharacterModelName" : "NumberLetter",
    //...
}
```

- If the `TextLineSpecification.CharacterModelName` is not specified:
- If the file path of CharacterModel
