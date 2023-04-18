---
layout: default-layout
Title: ErrorCode - Dynamsoft Core Enumerations
Description: The enumeration ErrorCode of Dynamsoft Core describes all error codes.
Keywords: Error code
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: ErrorCode
---

# Enumeration ErrorCode

`ErrorCode` describes the error code that can be output by the library.

<div class="sample-code-prefix template2"></div>
   >- JavaScript
   >- Android
   >- Objective-C
   >- Swift
   >- C
   >- C++
   >- C#
   >- Java
   >- Python
   >
>
```javascript
```
>
```java
```
>
```objc
```
>
```swift
```
>
```c
```
>
```cpp
typedef enum ErrorCode 
{
   /** Successful. */
   EC_OK = 0,
   /** -10000~-19999: Common error code. */
   /** Unknown error. */
   EC_UNKNOWN = -10000,
   /**Not enough memory to perform the operation. */
   EC_NO_MEMORY = -10001,
   /** Null pointer */
   EC_NULL_POINTER = -10002,
   /** License invalid. */
   EC_LICENSE_INVALID = -10003,
   /** License expired. */
   EC_LICENSE_EXPIRED = -10004,
   /** File not found. */
   EC_FILE_NOT_FOUND = -10005,
   /** The file type is not supported. */
   EC_FILE_TYPE_NOT_SUPPORTED = -10006,
   /** The BPP (Bits Per Pixel) is not supported. */
   EC_BPP_NOT_SUPPORTED = -10007,
   /** The index is invalid. */
   EC_INDEX_INVALID = -10008,
   /** The input region value parameter is invalid. */
   EC_CUSTOM_REGION_INVALID = -10010,
   /** Failed to read the image. */
   EC_IMAGE_READ_FAILED = -10012,
   /** Failed to read the TIFF image. */
   EC_TIFF_READ_FAILED = -10013,
   /** The DIB (Device-Independent Bitmaps) buffer is invalid. */
   EC_DIB_BUFFER_INVALID = -10018,
   /** Failed to read the PDF image. */
   EC_PDF_READ_FAILED = -10021,
   /** The PDF DLL is missing. */
   EC_PDF_DLL_MISSING = -10022,
   /** The page number is invalid. */
   EC_PAGE_NUMBER_INVALID = -10023,
   /** The custom size is invalid. */
   EC_CUSTOM_SIZE_INVALID = -10024,
   /** timeout. */
   EC_TIMEOUT = -10026,
   /** Json parse failed. */
   EC_JSON_PARSE_FAILED = -10030,
   /** Json type invalid. */
   EC_JSON_TYPE_INVALID = -10031,
   /** Json key invalid. */
   EC_JSON_KEY_INVALID = -10032,
   /** Json value invalid. */
   EC_JSON_VALUE_INVALID = -10033,
   /** Json name key missing. */
   EC_JSON_NAME_KEY_MISSING = -10034,
   /** The value of the key "Name" is duplicated. */
   EC_JSON_NAME_VALUE_DUPLICATED = -10035,
   /** Template name invalid. */
   EC_TEMPLATE_NAME_INVALID = -10036,
   /** The name reference is invalid. */
   EC_JSON_NAME_REFERENCE_INVALID = -10037,
   /** Parameter value invalid. */
   EC_PARAMETER_VALUE_INVALID = -10038,
   /** The domain of your current site does not match the domain bound in the current product key. */
   EC_DOMAIN_NOT_MATCH = -10039,
   /** The reserved info does not match the reserved info bound in the current product key. */
   EC_RESERVED_INFO_NOT_MATCH = -10040,
   /** The License DLL is missing. */
   EC_LICENSE_DLL_MISSING = -10042;
   /** The license key does not match the license content. */
   EC_LICENSE_KEY_NOT_MATCH = -10043,
   /** Failed to request the license content. */
   EC_REQUEST_FAILED = -10044,
   /** Failed to init the license. */
   EC_LICENSE_INIT_FAILED = -10045,
   /** Failed to set mode's argument. */
   EC_SET_MODE_ARGUMENT_ERROR = -10051,
   /** The license content is invalid. */
   EC_LICENSE_CONTENT_INVALID = -10052,
   /** The license key is invalid. */
   EC_LICENSE_KEY_INVALID = -10053,
   /** The license key has no remaining quota. */
   EC_LICENSE_DEVICE_RUNS_OUT = -10054,
   /** Failed to get mode's argument. */
   EC_GET_MODE_ARGUMENT_ERROR = -10055,
   /** The Intermediate Result Types license is invalid. */
   EC_IRT_LICENSE_INVALID = -10056,
   /** Failed to save file. */
   EC_FILE_SAVE_FAILED = -10058,
   /** The stage type is invalid. */
   EC_STAGE_TYPE_INVALID = -10059,
   /** The image orientation is invalid. */
   EC_IMAGE_ORIENTATION_INVALID = -10060,
   /** Complex tempalte can't be converted to simplified settings. */
   EC_CONVERT_COMPLEX_TEMPLATE_ERROR = -10061,
   /** Can't update settings at runtime. */
   EC_UPDATE_SETTINGS_AT_RUNTIME_FAILED = -10062,
   /** -20000~-29999: DLS license error code. */
   /** No license. */
   EC_NO_LICENSE = -20000,
   /** The Handshake Code is invalid. */
   EC_HANDSHAKE_CODE_INVALID = -20001,
   /** Failed to read or write license buffer. */
   EC_LICENSE_BUFFER_FAILED = -20002,
   /** Failed to synchronize license info with license server. */
   EC_LICENSE_SYNC_FAILED = -20003,
   /** Device dose not match with buffer. */
   EC_DEVICE_NOT_MATCH = -20004,
   /** Failed to bind device. */
   EC_BIND_DEVICE_FAILED = -20005,
   /** Interface InitLicenseFromDLS can not be used together with other license initiation interfaces. */
   EC_LICENSE_INTERFACE_CONFLICT = -20006,
   /** License Client dll is missing. */
   EC_LICENSE_CLIENT_DLL_MISSING = -20007,
   /** Instance count is over limit. */
   EC_INSTANCE_COUNT_OVER_LIMIT = -20008,
   /** Interface InitLicenseFromDLS has to be called before creating any SDK objects. */
   EC_LICENSE_INIT_SEQUENCE_FAILED = -20009,
   /** Trial License */
   EC_TRIAL_LICENSE = -20010,
   /** Failed to reach License Server. */
   EC_FAILED_TO_REACH_DLS = -20200,
   /** -30000~-39999: DBR error code. */
   /** The barcode format is invalid. */
   EC_BARCODE_FORMAT_INVALID = -30009,
   /** The QR Code license is invalid. */
   EC_QR_LICENSE_INVALID = -30016,
   /** The 1D Barcode license is invalid. */
   EC_1D_LICENSE_INVALID = -30017,
   /** The PDF417 license is invalid. */
   EC_PDF417_LICENSE_INVALID = -30019,
   /** The DATAMATRIX license is invalid. */
   EC_DATAMATRIX_LICENSE_INVALID = -30020,
   /** The custom module size is invalid. */
   EC_CUSTOM_MODULESIZE_INVALID = -30025,
   /** The AZTEC license is invalid. */
   EC_AZTEC_LICENSE_INVALID = -30041,
   /** The Patchcode license is invalid. */
   EC_PATCHCODE_LICENSE_INVALID = -30046,
   /** The Postal code license is invalid. */
   EC_POSTALCODE_LICENSE_INVALID = -30047,
   /** The DPM license is invalid. */
   EC_DPM_LICENSE_INVALID = -30048,
   /** The frame decoding thread already exists. */
   EC_FRAME_DECODING_THREAD_EXISTS = -30049,
   /** Failed to stop the frame decoding thread. */
   EC_STOP_DECODING_THREAD_FAILED = -30050,
   /** The Maxicode license is invalid. */
   EC_MAXICODE_LICENSE_INVALID = -30057,
   /** The GS1 Databar license is invalid. */
   EC_GS1_DATABAR_LICENSE_INVALID = -30058,
   /** The GS1 Composite code license is invalid. */
   EC_GS1_COMPOSITE_LICENSE_INVALID = -30059,
   /** The DotCode license is invalid. */
   EC_DOTCODE_LICENSE_INVALID = -30061,
   /** The Pharmacode license is invalid. */
   EC_PHARMACODE_LICENSE_INVALID = -30062,
   /** -40000~-49999: DLR error code */
   /** Character Model file is not found. */
   EC_CHARACTER_MODEL_FILE_NOT_FOUND = -40100,
   /** -50000~-59999: DDN error code. */
   /**No content has been detected. */
   EC_CONTENT_NOT_FOUND = -50056,
   /*The quardrilateral is invalid. */
   EC_QUADRILATERAL_INVALID = -50057,
   /** -60000~-69999: DCE error code. */
   /**-60000~-69999: DCE error code*/
   EC_CAMERA_MODULE_NOT_EXIST = -60003;
   EC_CAMERA_ID_NOT_EXIST = -60006;
   EC_NO_SENSOR = -60045;
   /**-70000~-79999: Panorama error code. */
   /**The panorama license is invalid. */
   EC_PANORAMA_LICENSE_INVALID = -70060,
   /** -80000~-89999: Reserved error code. */
   /**-90000~-99999: DCP error code. */
   /** The resource path is not exist. */
   EC_RESOURCE_PATH_NOT_EXIST = -90001,
   /** Failed to load resource. */
   EC_RESOURCE_LOAD_FAILED = -90002,
   /** The code specification is not found. */
   EC_CODE_SPECIFICATION_NOT_FOUND = -90003,
   /** The full code string is empty. */
   EC_FULL_CODE_EMPTY = -90004,
   /** Failed to preprocess the full code string */
   EC_FULL_CODE_PREPROCESS_FAILED = -90005,
   /** The license for parsing South Africa Driver License is invalid. */
   EC_ZA_DL_LICENSE_INVALID = -90006,
   /** The license for parsing North America DL/ID is invalid. */
   EC_AAMVA_DL_ID_LICENSE_INVALID = -90007,
   /** The license for parsing Aadhaar is invalid. */
   EC_AADHAAR_LICENSE_INVALID = -90008,
   /** The license for parsing Machine Readable Travel Documents is invalid. */
   EC_MRTD_LICENSE_INVALID = -90009,
   /** The license for parsing Vehicle Identification Number is invalid. */
   EC_VIN_LICENSE_INVALID = -90010,
   /** The license for parsing customized code type is invalid. */
   EC_CUSTOMIZED_CODE_TYPE_LICENSE_INVALID = -90011,
} ErrorCode;
```
>
```csharp
```
>
```java
```
>
```python
```