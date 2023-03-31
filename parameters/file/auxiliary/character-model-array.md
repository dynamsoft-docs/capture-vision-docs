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

`CharacterModels` are the model files that stores the specially trained algorithm for character recognizing. The character model files consist of

- Model files (Required): The files that stores the major character recognition models.
- Assist model files (Optional): Support the recognition when the result output by the major model doesn't match the RegEx.
- Filter files (Optional): Set which characters are included or excluded from the text line recognition.

<div align="center">
   <p><img src="../assets/character-model.png" alt="character-model" width="20%" /></p>
   <p>Example of CharacterModel files</p>
</div>

In the `CharacterModel` object, what you have to specify are:

- The folder where you save the models.
- The name of the model that you want to use.

```json
{
    "Name": "NumberLetter",
    "DirectoryPath" : "D:\\CharacterModel\\"
}
```

The library will be able to find all the related files that match the name you input including both the major models and the assist models.

> Note: The specified models will be read in memory before the process of character recognition. If assist models are not found in the folder, the xxx will be implemented instead when the result doesn't match the RegEx.

If you have requirements to exclude any characters, you can configure a filter file and add the file path to your `CharacterModel` object.

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
