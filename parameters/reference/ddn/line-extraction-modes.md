
# LineExtractionModes

Defines how to extract lines from the image.

`LEM_GENERAL`

Designed for the senarios where the document background colour is distinct from the environment background colour. In these scenarios, contours of the document bounaries are clear enough on the binary images. As a result, the line segments can be easily extracted from the image.

`LEM_MARGIN_BASED`

Designed for the senarios where the background colour is similar to the environment background colour. For these scenarios, it is hard to get distinct contours of document boundaries with general binarization process. When the mode `LEM_MARGIN_BASED` is enabled, the library will implement different parameters for the binarization mode to separate the document contents and the background areas. The line segments of the document boundaries will be extracted from the margin between document contents and the background areas.
