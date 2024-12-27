---
layout: default-layout
title: ErrorCode - Dynamsoft Core Enumerations
description: The enumeration ErrorCode of Dynamsoft Core describes all error codes.
keywords: Error code
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: ErrorCode
codeAutoHeight: true
---

# Enumeration ErrorCode

`ErrorCode` enumerates the specific error codes that the SDK may return, providing a systematic way to identify and handle errors encountered during its operation.

<div class="sample-code-prefix template2"></div>
   >- JavaScript
   >- Android
   >- Objective-C
   >- Swift
   >- C++
   >- C#
   >
>
```javascript
enum EnumErrorCode
{
    /** Operation completed successfully. */
    EC_OK = 0,
    // Common error codes range from -10000 to -19999
    /** An unspecified error occurred. */
    EC_UNKNOWN = -10000,
    /** The system does not have enough memory to perform the requested operation. */
    EC_NO_MEMORY = -10001,
    /** A null pointer was encountered where a valid pointer was required. */
    EC_NULL_POINTER = -10002,
    /** The provided license is not valid. */
    EC_LICENSE_INVALID = -10003,
    /** The provided license has expired. */
    EC_LICENSE_EXPIRED = -10004,
    /** The specified file could not be found. */
    EC_FILE_NOT_FOUND = -10005,
    /** The file type is not supported for processing. */
    EC_FILE_TYPE_NOT_SUPPORTED = -10006,
    /** The image's bits per pixel (BPP) is not supported. */
    EC_BPP_NOT_SUPPORTED = -10007,
    /** The specified index is out of the valid range. */
    EC_INDEX_INVALID = -10008,
    /** The specified custom region value is invalid or out of range. */
    EC_CUSTOM_REGION_INVALID = -10010,
    /** Failed to read the image due to an error in accessing or interpreting the image data. */
    EC_IMAGE_READ_FAILED = -10012,
    /** Failed to read a TIFF image, possibly due to corruption or unsupported format. */
    EC_TIFF_READ_FAILED = -10013,
    /** The provided DIB (Device-Independent Bitmaps) buffer is invalid or corrupted. */
    EC_DIB_BUFFER_INVALID = -10018,
    /** Failed to read a PDF image, possibly due to corruption or unsupported format. */
    EC_PDF_READ_FAILED = -10021,
    /** Required PDF processing DLL is missing. */
    EC_PDF_DLL_MISSING = -10022,
    /** The specified page number is invalid or out of bounds for the document. */
    EC_PAGE_NUMBER_INVALID = -10023,
    /** The specified custom size is invalid or not supported. */
    EC_CUSTOM_SIZE_INVALID = -10024,
    /** The operation timed out. */
    EC_TIMEOUT = -10026,
    /** Failed to parse JSON input. */
    EC_JSON_PARSE_FAILED = -10030,
    /** The JSON type is invalid for the expected context. */
    EC_JSON_TYPE_INVALID = -10031,
    /** The JSON key is invalid or unrecognized in the current context. */
    EC_JSON_KEY_INVALID = -10032,
    /** The JSON value is invalid for the specified key. */
    EC_JSON_VALUE_INVALID = -10033,
    /** The required "Name" key is missing in the JSON data. */
    EC_JSON_NAME_KEY_MISSING = -10034,
    /** The value of the "Name" key is duplicated and conflicts with existing data. */
    EC_JSON_NAME_VALUE_DUPLICATED = -10035,
    /** The template name is invalid or does not match any known template. */
    EC_TEMPLATE_NAME_INVALID = -10036,
    /** The reference made by the "Name" key is invalid or points to nonexistent data. */
    EC_JSON_NAME_REFERENCE_INVALID = -10037,
    /** The parameter value provided is invalid or out of the expected range. */
    EC_PARAMETER_VALUE_INVALID = -10038,
    /** The domain of the current site does not match the domain bound to the current product key. */
    EC_DOMAIN_NOT_MATCH = -10039,
    /** The reserved information does not match the reserved info bound to the current product key. */
    EC_RESERVED_INFO_NOT_MATCH = -10040,
    /** The license key does not match the license content. */
    EC_LICENSE_KEY_NOT_MATCH = -10043,
    /** Failed to request the license content from the server. */
    EC_REQUEST_FAILED = -10044,
    /** Failed to initialize the license. */
    EC_LICENSE_INIT_FAILED = -10045,
    /** Error setting the mode's argument, indicating invalid or incompatible arguments. */
    EC_SET_MODE_ARGUMENT_ERROR = -10051,
    /** The license content is invalid or corrupted. */
    EC_LICENSE_CONTENT_INVALID = -10052,
    /** The license key is invalid or does not match any known valid keys. */
    EC_LICENSE_KEY_INVALID = -10053,
    /** The license key has reached its maximum allowed usage and has no remaining quota. */
    EC_LICENSE_DEVICE_RUNS_OUT = -10054,
    /** Failed to retrieve the mode's argument, possibly due to invalid state or configuration. */
    EC_GET_MODE_ARGUMENT_ERROR = -10055,
    /** The Intermediate Result Types (IRT) license is invalid or not present. */
    EC_IRT_LICENSE_INVALID = -10056,
    /** Failed to save the file, possibly due to permissions, space, or an invalid path. */
    EC_FILE_SAVE_FAILED = -10058,
    /** The specified stage type is invalid or not supported in the current context. */
    EC_STAGE_TYPE_INVALID = -10059,
    /** The specified image orientation is invalid or not supported. */
    EC_IMAGE_ORIENTATION_INVALID = -10060,
    /** Failed to convert complex template to simplified settings, indicating a configuration or compatibility issue. */
    EC_CONVERT_COMPLEX_TEMPLATE_ERROR = -10061,
    /** Rejecting function call while capturing is in progress, to prevent conflicts or data corruption. */
    EC_CALL_REJECTED_WHEN_CAPTURING = -10062,
    /** The specified image source was not found, indicating a missing or inaccessible input source. */
    EC_NO_IMAGE_SOURCE = -10063,
    /** Failed to read the directory, possibly due to permissions, non-existence, or other access issues. */
    EC_READ_DIRECTORY_FAILED = -10064,
    /** A required module (e.g., DynamsoftBarcodeReader, DynamsoftLabelRecognizer) was not found. */
    EC_MODULE_NOT_FOUND = -10065,
    /** The operation does not support multi-page files; use FileFetcher for processing such files. */
    EC_MULTI_PAGES_NOT_SUPPORTED = -10066,
    /** Indicates an attempt to write to a file that already exists, with overwriting explicitly disabled. This error suggests the need for either enabling overwriting or ensuring unique file names to avoid conflicts. */
    EC_FILE_ALREADY_EXISTS = -10067,
    /** The specified file path does not exist and could not be created. This error could be due to insufficient permissions, a read-only filesystem, or other environmental constraints preventing file creation. */
    EC_CREATE_FILE_FAILED = -10068,
    /** The input ImageData object contains invalid parameters. This could be due to incorrect data types, out-of-range values, or improperly formatted data being passed to a function expecting ImageData. */
    EC_IMGAE_DATA_INVALID = -10069,
    // DLS license error codes range from -20000 to -29999
    /** Indicates no license is available or the license is not set. */
    EC_NO_LICENSE = -20000,
    /** The provided Handshake Code is invalid or does not match expected format. */
    EC_HANDSHAKE_CODE_INVALID = -20001,
    /** Encountered failures while attempting to read or write to the license buffer. */
    EC_LICENSE_BUFFER_FAILED = -20002,
    /** Synchronization with the license server failed, possibly due to network issues or server unavailability. */
    EC_LICENSE_SYNC_FAILED = -20003,
    /** The device attempting to use the license does not match the device specified in the license buffer. */
    EC_DEVICE_NOT_MATCH = -20004,
    /** Binding the device to the license failed, indicating possible issues with the license or device identifier. */
    EC_BIND_DEVICE_FAILED = -20005,
    /** The number of instances using the license exceeds the limit allowed by the license terms. */
    EC_INSTANCE_COUNT_OVER_LIMIT = -20008,
    /** InitLicenseFromDLS must be called before any SDK objects are created to ensure proper license initialization. */
    EC_LICENSE_INIT_SEQUENCE_FAILED = -20009,
    /** Indicates the license in use is a trial version with limited functionality or usage time. */
    EC_TRIAL_LICENSE = -20010,
    /** The system failed to reach the License Server, likely due to network connectivity issues. */
    EC_FAILED_TO_REACH_DLS = -20200,
    // DBR error codes range from -30000 to -39999
    /** The specified barcode format is invalid or unsupported. */
    EC_BARCODE_FORMAT_INVALID = -30009,
    /** The license for decoding QR Codes is invalid or not present. */
    EC_QR_LICENSE_INVALID = -30016,
    /** The license for decoding 1D barcodes is invalid or not present. */
    EC_1D_LICENSE_INVALID = -30017,
    /** The license for decoding PDF417 barcodes is invalid or not present. */
    EC_PDF417_LICENSE_INVALID = -30019,
    /** The license for decoding DataMatrix barcodes is invalid or not present. */
    EC_DATAMATRIX_LICENSE_INVALID = -30020,
    /** The specified custom module size for barcode generation is invalid or outside acceptable limits. */
    EC_CUSTOM_MODULESIZE_INVALID = -30025,
    /** The license for decoding Aztec barcodes is invalid or not present. */
    EC_AZTEC_LICENSE_INVALID = -30041,
    /** The license for decoding Patchcode barcodes is invalid or not present. */
    EC_PATCHCODE_LICENSE_INVALID = -30046,
    /** The license for decoding postal code formats is invalid or not present. */
    EC_POSTALCODE_LICENSE_INVALID = -30047,
    /** The license for Direct Part Marking (DPM) decoding is invalid or not present. */
    EC_DPM_LICENSE_INVALID = -30048,
    /** A frame decoding thread is already running, indicating a concurrent operation conflict. */
    EC_FRAME_DECODING_THREAD_EXISTS = -30049,
    /** Stopping the frame decoding thread failed, indicating potential issues with thread management. */
    EC_STOP_DECODING_THREAD_FAILED = -30050,
    /** The license for decoding MaxiCode barcodes is invalid or not present. */
    EC_MAXICODE_LICENSE_INVALID = -30057,
    /** The license for decoding GS1 DataBar barcodes is invalid or not present. */
    EC_GS1_DATABAR_LICENSE_INVALID = -30058,
    /** The license for decoding GS1 Composite codes is invalid or not present. */
    EC_GS1_COMPOSITE_LICENSE_INVALID = -30059,
    /** The license for decoding DotCode barcodes is invalid or not present. */
    EC_DOTCODE_LICENSE_INVALID = -30061,
    /** The license for decoding Pharmacode barcodes is invalid or not present. */
    EC_PHARMACODE_LICENSE_INVALID = -30062,
    // DLR error codes range from -40000 to -49999
    /** Indicates that the required character model file was not found, possibly due to incorrect paths or missing files. */
    EC_CHARACTER_MODEL_FILE_NOT_FOUND = -40100,
    // DDN error codes range from -50000 to -59999
    /** The specified quadrilateral is invalid, potentially due to incorrect points or an unprocessable shape. */
    EC_QUADRILATERAL_INVALID = -50057,
    // Panorama error codes range from -70000 to -79999
    /** The license for generating or processing panoramas is invalid or missing. */
    EC_PANORAMA_LICENSE_INVALID = -70060,
    // Reserved error codes range from -80000 to -89999
    // DCP error codes range from -90000 to -99999
    /** The specified resource path does not exist, indicating a missing directory or incorrect path specification. */
    EC_RESOURCE_PATH_NOT_EXIST = -90001,
    /** Failed to load the specified resource, which might be due to missing files, access rights, or other issues preventing loading. */
    EC_RESOURCE_LOAD_FAILED = -90002,
    /** The code specification required for processing was not found, indicating a missing or incorrect specification. */
    EC_CODE_SPECIFICATION_NOT_FOUND = -90003,
    /** The full code string provided is empty, indicating no data was provided for processing. */
    EC_FULL_CODE_EMPTY = -90004,
    /** Preprocessing the full code string failed, possibly due to invalid format, corruption, or unsupported features. */
    EC_FULL_CODE_PREPROCESS_FAILED = -90005,
    /** The license required for parsing South Africa Driver License data is invalid or not present. */
    EC_ZA_DL_LICENSE_INVALID = -90006,
    /** The license required for parsing North America DL/ID (AAMVA) data is invalid or not present. */
    EC_AAMVA_DL_ID_LICENSE_INVALID = -90007,
    /** The license required for parsing Aadhaar data is invalid or not present. */
    EC_AADHAAR_LICENSE_INVALID = -90008,
    /** The license required for parsing Machine Readable Travel Documents (MRTD) is invalid or not present. */
    EC_MRTD_LICENSE_INVALID = -90009,
    /** The license required for parsing Vehicle Identification Number (VIN) data is invalid or not present. */
    EC_VIN_LICENSE_INVALID = -90010,
    /** The license required for parsing customized code types is invalid or not present. */
    EC_CUSTOMIZED_CODE_TYPE_LICENSE_INVALID = -90011
}
```
>
```java
@Retention(RetentionPolicy.CLASS)
public @interface EnumErrorCode
{
   /** Successful. */
   public static final int EC_OK = 0;
   /** -10000~-19999: Common error code. */
   /** Unknown error. */
   public static final int EC_UNKNOWN = -10000,
   /**Not enough memory to perform the operation. */
   public static final int EC_NO_MEMORY = -10001,
   /** Null pointer */
   public static final int EC_NULL_POINTER = -10002,
   /** License invalid. */
   public static final int EC_LICENSE_INVALID = -10003,
   /** License expired. */
   public static final int EC_LICENSE_EXPIRED = -10004,
   /** File not found. */
   public static final int EC_FILE_NOT_FOUND = -10005,
   /** The file type is not supported. */
   public static final int EC_FILE_TYPE_NOT_SUPPORTED = -10006,
   /** The BPP (Bits Per Pixel) is not supported. */
   public static final int EC_BPP_NOT_SUPPORTED = -10007,
   /** The index is invalid. */
   public static final int EC_INDEX_INVALID = -10008,
   /** The input region value parameter is invalid. */
   public static final int EC_CUSTOM_REGION_INVALID = -10010,
   /** Failed to read the image. */
   public static final int EC_IMAGE_READ_FAILED = -10012,
   /** Failed to read the TIFF image. */
   public static final int EC_TIFF_READ_FAILED = -10013,
   /** The DIB (Device-Independent Bitmaps) buffer is invalid. */
   public static final int EC_DIB_BUFFER_INVALID = -10018,
   /** Failed to read the PDF image. */
   public static final int EC_PDF_READ_FAILED = -10021,
   /** The PDF DLL is missing. */
   public static final int EC_PDF_DLL_MISSING = -10022,
   /** The page number is invalid. */
   public static final int EC_PAGE_NUMBER_INVALID = -10023,
   /** The custom size is invalid. */
   public static final int EC_CUSTOM_SIZE_INVALID = -10024,
   /** timeout. */
   public static final int EC_TIMEOUT = -10026,
   /** Json parse failed. */
   public static final int EC_JSON_PARSE_FAILED = -10030,
   /** Json type invalid. */
   public static final int EC_JSON_TYPE_INVALID = -10031,
   /** Json key invalid. */
   public static final int EC_JSON_KEY_INVALID = -10032,
   /** Json value invalid. */
   public static final int EC_JSON_VALUE_INVALID = -10033,
   /** Json name key missing. */
   public static final int EC_JSON_NAME_KEY_MISSING = -10034,
   /** The value of the key "Name" is duplicated. */
   public static final int EC_JSON_NAME_VALUE_DUPLICATED = -10035,
   /** Template name invalid. */
   public static final int EC_TEMPLATE_NAME_INVALID = -10036,
   /** The name reference is invalid. */
   public static final int EC_JSON_NAME_REFERENCE_INVALID = -10037,
   /** Parameter value invalid. */
   public static final int EC_PARAMETER_VALUE_INVALID = -10038,
   /** The domain of your current site does not match the domain bound in the current product key. */
   public static final int EC_DOMAIN_NOT_MATCH = -10039,
   /** The reserved info does not match the reserved info bound in the current product key. */
   public static final int EC_RESERVED_INFO_NOT_MATCH = -10040,
   /** The license key does not match the license content. */
   public static final int EC_LICENSE_KEY_NOT_MATCH = -10043,
   /** Failed to request the license content. */
   public static final int EC_REQUEST_FAILED = -10044,
   /** Failed to init the license. */
   public static final int EC_LICENSE_INIT_FAILED = -10045,
   /** Failed to set mode's argument. */
   public static final int EC_SET_MODE_ARGUMENT_ERROR = -10051,
   /** The license content is invalid. */
   public static final int EC_LICENSE_CONTENT_INVALID = -10052,
   /** The license key is invalid. */
   public static final int EC_LICENSE_KEY_INVALID = -10053,
   /** The license key has no remaining quota. */
   public static final int EC_LICENSE_DEVICE_RUNS_OUT = -10054,
   /** Failed to get mode's argument. */
   public static final int EC_GET_MODE_ARGUMENT_ERROR = -10055,
   /** The Intermediate Result Types license is invalid. */
   public static final int EC_IRT_LICENSE_INVALID = -10056,
   /** Failed to save file. */
   public static final int EC_FILE_SAVE_FAILED = -10058,
   /** The stage type is invalid. */
   public static final int EC_STAGE_TYPE_INVALID = -10059,
   /** The image orientation is invalid. */
   public static final int EC_IMAGE_ORIENTATION_INVALID = -10060,
   /** Complex tempalte can't be converted to simplified settings. */
   public static final int EC_CONVERT_COMPLEX_TEMPLATE_ERROR = -10061,
   /** Reject function call while capturing in progress.*/
   public static final int EC_CALL_REJECTED_WHEN_CAPTURING = -10062,
   /**The input image source was not found.*/
   public static final int EC_NO_IMAGE_SOURCE = -10063,
   /**Failed to read directory.*/
   public static final int EC_READ_DIRECTORY_FAILED = -10064,
   /**[Name] Module not found.*/
   /**Name : */
   /**DynamsoftBarcodeReader*/
   /**DynamsoftLabelRecognizer*/
   /**DynamsoftDocumentNormalizer*/
   public static final int EC_MODULE_NOT_FOUND = -10065,
   /**The file already exists but overwriting is disabled.*/
   public static final int EC_FILE_ALREADY_EXISTS = -10067,
   /**The file path does not exist but cannot be created, or cannot be created for any other reason.*/
   public static final int EC_CREATE_FILE_FAILED = -10068,
   /**The input ImageData object contains invalid parameter(s).*/
   public static final int EC_IMGAE_DATA_INVALID = -10069,
   /**The size of the input image do not meet the requirements.*/
   public static final int EC_IMAGE_SIZE_NOT_MATCH = -10070,
   /**The pixel format of the input image do not meet the requirements.*/
   public static final int EC_IMAGE_PIXEL_FORMAT_NOT_MATCH = -10071,
   /**The section level result is irreplaceable.*/
   public static final int EC_SECTION_LEVEL_RESULT_IRREPLACEABLE = -10072,
   /** -20000~-29999: DLS license error code. */
   /** No license. */
   public static final int EC_NO_LICENSE = -20000,
   /** The Handshake Code is invalid. */
   public static final int EC_HANDSHAKE_CODE_INVALID = -20001,
   /** Failed to read or write license buffer. */
   public static final int EC_LICENSE_BUFFER_FAILED = -20002,
   /** Failed to synchronize license info with license server. */
   public static final int EC_LICENSE_SYNC_FAILED = -20003,
   /** Device dose not match with buffer. */
   public static final int EC_DEVICE_NOT_MATCH = -20004,
   /** Failed to bind device. */
   public static final int EC_BIND_DEVICE_FAILED = -20005,
   /** Instance count is over limit. */
   public static final int EC_INSTANCE_COUNT_OVER_LIMIT = -20008,
   /** Trial License */
   public static final int EC_TRIAL_LICENSE = -20010,
   /** Failed to reach License Server. */
   public static final int EC_FAILED_TO_REACH_DLS = -20200,
   /** -30000~-39999: DBR error code. */
   /** The barcode format is invalid. */
   public static final int EC_BARCODE_FORMAT_INVALID = -30009,
   /** The QR Code license is invalid. */
   public static final int EC_QR_LICENSE_INVALID = -30016,
   /** The 1D Barcode license is invalid. */
   public static final int EC_1D_LICENSE_INVALID = -30017,
   /** The PDF417 license is invalid. */
   public static final int EC_PDF417_LICENSE_INVALID = -30019,
   /** The DATAMATRIX license is invalid. */
   public static final int EC_DATAMATRIX_LICENSE_INVALID = -30020,
   /** The custom module size is invalid. */
   public static final int EC_CUSTOM_MODULESIZE_INVALID = -30025,
   /** The AZTEC license is invalid. */
   public static final int EC_AZTpublic static final int EC_LICENSE_INVALID = -30041,
   /** The Patchcode license is invalid. */
   public static final int EC_PATCHCODE_LICENSE_INVALID = -30046,
   /** The Postal code license is invalid. */
   public static final int EC_POSTALCODE_LICENSE_INVALID = -30047,
   /** The DPM license is invalid. */
   public static final int EC_DPM_LICENSE_INVALID = -30048,
   /** The frame decoding thread already exists. */
   public static final int EC_FRAME_DECODING_THREAD_EXISTS = -30049,
   /** Failed to stop the frame decoding thread. */
   public static final int EC_STOP_DECODING_THREAD_FAILED = -30050,
   /** The Maxicode license is invalid. */
   public static final int EC_MAXICODE_LICENSE_INVALID = -30057,
   /** The GS1 Databar license is invalid. */
   public static final int EC_GS1_DATABAR_LICENSE_INVALID = -30058,
   /** The GS1 Composite code license is invalid. */
   public static final int EC_GS1_COMPOSITE_LICENSE_INVALID = -30059,
   /** The DotCode license is invalid. */
   public static final int EC_DOTCODE_LICENSE_INVALID = -30061,
   /** The Pharmacode license is invalid. */
   public static final int EC_PHARMACODE_LICENSE_INVALID = -30062,
   /** -40000~-49999: DLR error code */
   /** Character Model file is not found. */
   public static final int EC_CHARACTER_MODEL_FILE_NOT_FOUND = -40100,
   /**There is a conflict in the layout of TextLineGroup. */
   public static final int EC_TEXT_LINE_GROUP_LAYOUT_CONFLICT = -40101,
   /**There is a conflict in the regex of TextLineGroup. */
   public static final int EC_TEXT_LINE_GROUP_REGEX_CONFLICT = -40102,
   /** -50000~-59999: DDN error code. */
   /**No content has been detected. */
   public static final int EC_CONTENT_NOT_FOUND = -50056,
   /*The quardrilateral is invalid. */
   public static final int EC_QUADRILATERAL_INVALID = -50057,
   /** -60000~-69999: DCE error code. */
   /**-60000~-69999: DCE error code*/
   /** The camera module is not exist. */
   public static final int EC_CAMERA_MODULE_NOT_EXIST = -60003;
   /** The camera id does not exist. */
   public static final int EC_CAMERA_ID_NOT_EXIST = -60006;
   /** The sensor does not exist. */
   public static final int EC_NO_SENSOR = -60045;
   /**-70000~-79999: Panorama error code. */
   /**The panorama license is invalid. */
   public static final int EC_PANORAMA_LICENSE_INVALID = -70060,
   /** -80000~-89999: Reserved error code. */
   /**-90000~-99999: DCP error code. */
   /** The resource path is not exist. */
   public static final int EC_RESOURCE_PATH_NOT_EXIST = -90001,
   /** Failed to load resource. */
   public static final int EC_RESOURCE_LOAD_FAILED = -90002,
   /** The code specification is not found. */
   public static final int EC_CODE_SPECIFICATION_NOT_FOUND = -90003,
   /** The full code string is empty. */
   public static final int EC_FULL_CODE_EMPTY = -90004,
   /** Failed to preprocess the full code string */
   public static final int EC_FULL_CODE_PREPROCESS_FAILED = -90005,
   /** The license for parsing South Africa Driver License is invalid. */
   public static final int EC_ZA_DL_LICENSE_INVALID = -90006,
   /** The license for parsing North America DL/ID is invalid. */
   public static final int EC_AAMVA_DL_ID_LICENSE_INVALID = -90007,
   /** The license for parsing Aadhaar is invalid. */
   public static final int EC_AADHAAR_LICENSE_INVALID = -90008,
   /** The license for parsing Machine Readable Travel Documents is invalid. */
   public static final int EC_MRTD_LICENSE_INVALID = -90009,
   /** The license for parsing Vehicle Identification Number is invalid. */
   public static final int EC_VIN_LICENSE_INVALID = -90010,
   /** The license for parsing customized code type is invalid. */
   public static final int EC_CUSTOMIZED_CODE_TYPE_LICENSE_INVALID = -90011,
} ErrorCode;
```
>
```objc
typedef NS_ERROR_ENUM(DSErrorDomain, DSError) {
   /**Successful. */
   DSErrorOK                               = 0,
   /**Unknown error. */
   DSErrorUnknown                          = -10000,
   /**Not enough memory to perform the operation. */
   DSErrorNoMemory                         = -10001,
   /**Null pointer */
   DSErrorNullPointer                      = -10002,
   /**License invalid*/
   DSErrorLicenseInvalid                   = -10003,
   /**License expired*/
   DSErrorLicenseExpired                   = -10004,
   /**File not found*/
   DSErrorFileNotFound                     = -10005,
   /**The file type is not supported. */
   DSErrorFiletypeNotSupported             = -10006,
   /**The BPP (Bits Per Pixel) is not supported. */
   DSErrorBPPNotSupported                  = -10007,
   /**Failed to read the image. */
   DSErrorImageReadFailed                  = -10012,
   /**Failed to read the TIFF image. */
   DSErrorTiffReadFailed                   = -10013,
   /**The DIB (Device-Independent Bitmaps) buffer is invalid. */
   DSErrorDIBBufferInvalid                 = -10018,
   /**Failed to read the PDF image. */
   DSErrorPdfReadFailed                    = -10021,
   /**The PDF DLL is missing. */
   DSErrorPdfDllMissing                    = -10022,
   /**The page number is invalid. */
   DSErrorPageNumberInvalid                = -10023,
   /**The custom size is invalid. */
   DSErrorCustomSizeInvalid                = -10024,
   /** timeout. */
   DSErrorTimeout                          = -10026,
   /**Json parse failed*/
   DSErrorJsonParseFailed                  = -10030,
   /**Json type invalid*/
   DSErrorJsonTypeInvalid                  = -10031,
   /**Json key invalid*/
   DSErrorJsonKeyInvalid                   = -10032,
   /**Json value invalid*/
   DSErrorJsonValueInvalid                 = -10033,
   /**Json name key missing*/
   DSErrorJsonNameKeyMissing               = -10034,
   /**The value of the key "Name" is duplicated.*/
   DSErrorJsonNameValueDuplicated          = -10035,
   /**Template name invalid*/
   DSErrorTemplateNameInvalid              = -10036,
   /**The name reference is invalid.*/
   DSErrorJsonNameReferenceInvalid         = -10037,
   /**Parameter value invalid*/
   DSErrorParameterValueInvalid            = -10038,
   /**The domain of your current site does not match the domain bound in the current product key.*/
   DSErrorDomainNotMatch                   = -10039,
   /**The reserved info does not match the reserved info bound in the current product key.*/
   DSErrorReservedInfoNotMatch             = -10040,
   /**The license key does not match the license content.*/
   DSErrorLicenseKeyNotMatch               = -10043,
   /**Failed to request the license content.*/
   DSErrorRequestFailed                    = -10044,
   /**Failed to init the license.*/
   DSErrorLicenseInitFailed                = -10045,
   /**Failed to set mode's argument.*/
   DSErrorSetModeArgumentError             = -10051,
   /**The license content is invalid.*/
   DSErrorLicenseContentInvalid            = -10052,
   /**The license key is invalid.*/
   DSErrorLicenseKeyInvalid                = -10053,
   /**The license key has no remaining quota.*/
   DSErrorLicenseDeviceRunsOut             = -10054,
   /**Failed to get mode's argument.*/
   DSErrorGetModeArgumentError             = -10055,
   /**The Intermediate Result Types license is invalid.*/
   DSErrorIrtLicenseInvalid                = -10056,
   /**Failed to save file.*/
   DSErrorFileSaveFailed                   = -10058,
   /**The stage type is invalid.*/
   DSErrorStageTypeInvalid                 = -10059,
   /**The image orientation is invalid.*/
   DSErrorImageOrientationInvalid          = -10060,
   /**Failed to convert complex tempalte to simplified settings.*/
   DSErrorConvertComplexTemplateError      = -10061,
   /**Reject function call while capturing in progress.*/
   DSErrorCallRejectedWhenCapturing        = -10062,
   /**The input image source was not found.*/
   DSErrorNoImageSource                    = -10063,
   /**Failed to read directory.*/
   DSErrorReadDirectoryFailed              = -10064,
   /**[Name] Module not found.*/
   /**Name : */
   /**DynamsoftBarcodeReader*/
   /**DynamsoftLabelRecognizer*/
   /**DynamsoftDocumentNormalizer*/
   DSErrorModuleNotFound                   = -10065,
   /**The file already exists but overwriting is disabled.*/
   DSErrorFileAlreadyExists                = -10067,
   /**The file path does not exist but cannot be created, or cannot be created for any other reason.*/
   DSErrorCreateFileFailed                 = -10068,
   /**The input ImageData object contains invalid parameter(s).*/
   DSErrorImageDataInvalid                 = -10069,
   /**The size of the input image does not meet the requirements.*/
   DSErrorImageSizeNotMatch                    = -10070,
   /**The pixel format of the input image does not meet the requirements.*/
   DSErrorImagePixelFormatNotMatch             = -10071,
   /**The section level result is irreplaceable.*/
   DSErrorSectionLevelResultIrreplaceable      = -10072,
   /**No license.*/
   DSErrorNoLicense                        = -20000,
   /**The handshake code is invalid. */
   DSErrorHandshakeCodeInvalid             = -20001,
   /**Failed to read or write license cache. */
   DSErrorLicenseBufferFailed              = -20002,
   /**Falied to synchronize license info wirh license tracking server. */
   DSErrorLicenseSyncFailed                = -20003,
   /**Device does not match with license buffer. */
   DSErrorDeviceNotMatch                   = -20004,
   /**Falied to bind device. */
   DSErrorBindDeviceFailed                 = -20005,
   /**Install.*/
   DSErrorInstanceCountOverLimit           = -20008,
   /**Trial License*/
   DSErrorTrialLicense                     = -20010,
   /**The license is not valid for current version*/
   DSErrorLicenseVersionNotMatch           = -20011,
   /**Failed to reach License Tracking Server.*/
   DSErrorFailedToReachDLS                 = -20200
   /** -30000~-39999: DBR error code. */
   /** The barcode format is invalid. */
   DSErrorBarcodeFormatInvalid             = -30009,
   /** The QR Code license is invalid. */
   DSErrorQRLicenseInvalid                 = -30016,
   /** The 1D Barcode license is invalid. */
   DSError1DLicenseInvalid                 = -30017,
   /** The PDF417 license is invalid. */
   DSErrorPDF417LicenseInvalid             = -30019,
   /** The DATAMATRIX license is invalid. */
   DSErrorDATAMATRIXLicenseInvalid         = -30020,
   /** The custom module size is invalid. */
   DSErrorCustomModuleSizeInvalid          = -30025,
   /** The AZTEC license is invalid. */
   DSErrorAztecLicenseInvalid              = -30041,
   /** The Patchcode license is invalid. */
   DSErrorPatchCodeLicenseInvalid          = -30046,
   /** The Postal code license is invalid. */
   DSErrorPostalCodeLicenseInvalid         = -30047,
   /** The DPM license is invalid. */
   DSErrorDPMLicenseInvalid                = -30048,
   /** The frame decoding thread already exists. */
   DSErrorFrameDecodingThreadExists        = -30049,
   /** Failed to stop the frame decoding thread. */
   DSErrorStopDecodingThreadFailed         = -30050,
   /** The Maxicode license is invalid. */
   DSErrorMaxiCodeLicenseInvalid           = -30057,
   /** The GS1 Databar license is invalid. */
   DSErrorGS1DatabarLicenseInvalid         = -30058,
   /** The GS1 Composite code license is invalid. */
   DSErrorGS1CompositeLicenseInvalid       = -30059,
   /** The DotCode license is invalid. */
   DSErrorDotCodeLicenseInvalid            = -30061,
   /** The Pharmacode license is invalid. */
   DSErrorPharmaCodeLicenseInvalid         = -30062,
   /** -40000~-49999: DLR error code */
   /** Character Model file is not found. */
   DSErrorCharacterModelFileNotFound       = -40100,
   /** There is a conflict in the layout of TextLineGroup. */
   DSErrorTextLineGroupLayoutConflict          = -40101,
   /** There is a conflict in the regex of TextLineGroup. */
   DSErrorTextLineGroupRegexConflict           = -40102,
   /** -50000~-59999: DDN error code. */
   /**No content has been detected. */
   DSErrorContentNotFound                  = -50056,
   /*The quardrilateral is invalid. */
   DSErrorQuardrilateralInvalid            = -50057,
   /** -60000~-69999: DCE error code. */
   DSErrorCameraModelNotExist              = -60003,
   DSErrorCameraIDNotExist                 = -60006,
   DSErrorNoSensor                         = -60045,
   /**-70000~-79999: Panorama error code. */
   /**The panorama license is invalid. */
   DSErrorPanoramaLicenseInvalid           = -70060,
   /** -80000~-89999: Reserved error code. */
   /**-90000~-99999: DCP error code. */
   /** The resource path is not exist. */
   DSErrorResourcePathNotExist             = -90001,
   /** Failed to load resource. */
   DSErrorResourceLoadFailed               = -90002,
   /** The code specification is not found. */
   DSErrorCodeSpecificationNotFound        = -90003,
   /** The full code string is empty. */
   DSErrorFullCodeEmpty                    = -90004,
   /** Failed to preprocess the full code string */
   DSErrorFullCodePreprocessFailed         = -90005,
   /** The license for parsing South Africa Driver License is invalid. */
   DSErrorZADLLicenseInvalid               = -90006,
   /** The license for parsing North America DL/ID is invalid. */
   DSErrorAAMVADLIDLicenseInvalid          = -90007,
   /** The license for parsing Aadhaar is invalid. */
   DSErrorAADHAARLicenseInvalid            = -90008,
   /** The license for parsing Machine Readable Travel Documents is invalid. */
   DSErrorMRTDLicenseInvalid               = -90009,
   /** The license for parsing Vehicle Identification Number is invalid. */
   DSErrorVINLicenseInvalid                = -90010,
   /** The license for parsing customized code type is invalid. */
   DSErrorCustomizedCodeTypeLicenseInvalid = -90011,
};
```
>
```swift
public enum ErrorCode : Int
{
   /**Successful. */
   oK                               = 0
   /**Unknown error. */
   unknown                          = -10000
   /**Not enough memory to perform the operation. */
   noMemory                         = -10001
   /**Null pointer */
   nullPointer                      = -10002
   /**License invalid*/
   licenseInvalid                   = -10003
   /**License expired*/
   licenseExpired                   = -10004
   /**File not found*/
   fileNotFound                     = -10005
   /**The file type is not supported. */
   filetypeNotSupported             = -10006
   /**The BPP (Bits Per Pixel) is not supported. */
   bppNotSupported                  = -10007
   /**Failed to read the image. */
   imageReadFailed                  = -10012
   /**Failed to read the TIFF image. */
   tiffReadFailed                   = -10013
   /**The DIB (Device-Independent Bitmaps) buffer is invalid. */
   dibBufferInvalid                     = -10018,
   /**Failed to read the PDF image. */
   pdfReadFailed                    = -10021
   /**The PDF DLL is missing. */
   pdfDllMissing                    = -10022
   /**The page number is invalid. */
   pageNumberInvalid                = -10023
   /**The custom size is invalid. */
   customSizeInvalid                = -10024
   /** timeout. */
   timeout                          = -10026
   /**Json parse failed*/
   jsonParseFailed                  = -10030
   /**Json type invalid*/
   jsonTypeInvalid                  = -10031
   /**Json key invalid*/
   jsonKeyInvalid                   = -10032
   /**Json value invalid*/
   jsonValueInvalid                 = -10033
   /**Json name key missing*/
   jsonNameKeyMissing               = -10034
   /**The value of the key "Name" is duplicated.*/
   jsonNameValueDuplicated          = -10035
   /**Template name invalid*/
   templateNameInvalid              = -10036
   /**The name reference is invalid.*/
   jsonNameReferenceInvalid         = -10037
   /**Parameter value invalid*/
   parameterValueInvalid            = -10038
   /**The domain of your current site does not match the domain bound in the current product key.*/
   domainNotMatch                   = -10039
   /**The reserved info does not match the reserved info bound in the current product key.*/
   reservedInfoNotMatch             = -10040
   /**The license key does not match the license content.*/
   licenseKeyNotMatch               = -10043
   /**Failed to request the license content.*/
   requestFailed                    = -10044
   /**Failed to init the license.*/
   licenseInitFailed                = -10045
   /**Failed to set mode's argument.*/
   setModeArgumentError             = -10051
   /**The license content is invalid.*/
   licenseContentInvalid            = -10052
   /**The license key is invalid.*/
   licenseKeyInvalid                = -10053
   /**The license key has no remaining quota.*/
   licenseDeviceRunsOut             = -10054
   /**Failed to get mode's argument.*/
   getModeArgumentError             = -10055
   /**The Intermediate Result Types license is invalid.*/
   irtLicenseInvalid                = -10056
   /**Failed to save file.*/
   fileSaveFailed                   = -10058
   /**The stage type is invalid.*/
   stageTypeInvalid                 = -10059
   /**The image orientation is invalid.*/
   imageOrientationInvalid          = -10060
   /**Failed to convert complex tempalte to simplified settings.*/
   convertComplexTemplateError      = -10061
   /**Reject function call while capturing in progress.*/
   callRejectedWhenCapturing        = -10062
   /**The input image source was not found.*/
   noImageSource                    = -10063
   /**Failed to read directory.*/
   readDirectoryFailed              = -10064
   /**[Name] Module not found.*/
   /**Name : */
   /**DynamsoftBarcodeReader*/
   /**DynamsoftLabelRecognizer*/
   /**DynamsoftDocumentNormalizer*/
   moduleNotFound                   = -10065
   /**The file already exists but overwriting is disabled.*/
   fileAlreadyExists                = -10067
   /**The file path does not exist but cannot be created, or cannot be created for any other reason.*/
   createFileFailed                 = -10068
   /**The input ImageData object contains invalid parameter(s).*/
   imageDataInvalid                 = -10069
   /**The size of the input image does not meet the requirements.*/
   imageSizeNotMatch                = -10070
   /**The pixel format of the input image does not meet the requirements.*/
   imagePixelFormatNotMatch         = -10071
   /**The section level result is irreplaceable.*/
   sectionLevelResultIrreplaceable  = -10072
   /**No license.*/
   noLicense                        = -20000
   /**The handshake code is invalid. */
   handshakeCodeInvalid             = -20001
   /**Failed to read or write license cache. */
   licenseBufferFailed              = -20002
   /**Falied to synchronize license info wirh license tracking server. */
   licenseSyncFailed                = -20003
   /**Device does not match with license buffer. */
   deviceNotMatch                   = -20004
   /**Falied to bind device. */
   bindDeviceFailed                 = -20005
   /**Install.*/
   instanceCountOverLimit           = -20008
   /**Trial License*/
   trialLicense                     = -20010
   /**The license is not valid for current version*/
   licenseVersionNotMatch           = -20011
   /**Failed to reach License Tracking Server.*/
   failedToReachDLS                 = -20200
   /** -30000~-39999: DBR error code. */
   /** The barcode format is invalid. */
   barcodeFormatInvalid             = -30009
   /** The QR Code license is invalid. */
   qrLicenseInvalid                 = -30016
   /** The 1D Barcode license is invalid. */
   1DLicenseInvalid                 = -30017
   /** The PDF417 license is invalid. */
   pdf417LicenseInvalid             = -30019
   /** The DATAMATRIX license is invalid. */
   dataMatrixLicenseInvalid         = -30020
   /** The custom module size is invalid. */
   customModuleSizeInvalid          = -30025
   /** The AZTEC license is invalid. */
   aztecLicenseInvalid              = -30041
   /** The Patchcode license is invalid. */
   patchCodeLicenseInvalid          = -30046
   /** The Postal code license is invalid. */
   postalCodeLicenseInvalid         = -30047
   /** The DPM license is invalid. */
   dpmLicenseInvalid                = -30048
   /** The frame decoding thread already exists. */
   frameDecodingThreadExists        = -30049
   /** Failed to stop the frame decoding thread. */
   stopDecodingThreadFailed         = -30050
   /** The Maxicode license is invalid. */
   maxiCodeLicenseInvalid           = -30057
   /** The GS1 Databar license is invalid. */
   gs1DatabarLicenseInvalid         = -30058
   /** The GS1 Composite code license is invalid. */
   gs1CompositeLicenseInvalid       = -30059
   /** The DotCode license is invalid. */
   dotCodeLicenseInvalid            = -30061
   /** The Pharmacode license is invalid. */
   pharmaCodeLicenseInvalid         = -30062
   /** -40000~-49999: DLR error code */
   /** Character Model file is not found. */
   characterModelFileNotFound       = -40100
   /** There is a conflict in the layout of TextLineGroup. */
   textLineGroupLayoutConflict      = -40101
   /** There is a conflict in the regex of TextLineGroup. */
   textLineGroupRegexConflict       = -40102
   /** -50000~-59999: DDN error code. */
   /** No content has been detected. */
   contentNotFound                  = -50056
   /*The quardrilateral is invalid. */
   quardrilateralInvalid            = -50057
   /** -60000~-69999: DCE error code. */
   /** The camera module is not exist. */
   cameraModelNotExist              = -60003
   /** The camera id does not exist. */
   cameraIDNotExist                 = -60006
   /** The sensor does not exist. */
   noSensor                         = -60045
   /**-70000~-79999: Panorama error code. */
   /**The panorama license is invalid. */
   panoramaLicenseInvalid           = -70060
   /** -80000~-89999: Reserved error code. */
   /**-90000~-99999: DCP error code. */
   /** The resource path is not exist. */
   resourcePathNotExist             = -90001
   /** Failed to load resource. */
   resourceLoadFailed               = -90002
   /** The code specification is not found. */
   codeSpecificationNotFound        = -90003
   /** The full code string is empty. */
   fullCodeEmpty                    = -90004
   /** Failed to preprocess the full code string */
   fullCodePreprocessFailed         = -90005
   /** The license for parsing South Africa Driver License is invalid. */
   zadlLicenseInvalid               = -90006
   /** The license for parsing North America DL/ID is invalid. */
   aamvadlidLicenseInvalid          = -90007
   /** The license for parsing Aadhaar is invalid. */
   aadhaarLicenseInvalid            = -90008
   /** The license for parsing Machine Readable Travel Documents is invalid. */
   mrtdLicenseInvalid               = -90009
   /** The license for parsing Vehicle Identification Number is invalid. */
   vinLicenseInvalid                = -90010
   /** The license for parsing customized code type is invalid. */
   customizedCodeTypeLicenseInvalid = -90011
}
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
   /** Reject function call while capturing in progress.*/
   EC_CALL_REJECTED_WHEN_CAPTURING = -10062,
   /**The input image source was not found.*/
   EC_NO_IMAGE_SOURCE = -10063,
   /**Failed to read directory.*/
   EC_READ_DIRECTORY_FAILED = -10064,
   /**[Name] Module not found.*/
   /**Name : */
   /**DynamsoftBarcodeReader*/
   /**DynamsoftLabelRecognizer*/
   /**DynamsoftDocumentNormalizer*/
   EC_MODULE_NOT_FOUND = -10065,
   /**The file already exists but overwriting is disabled.*/
   EC_FILE_ALREADY_EXISTS = -10067,
   /**The file path does not exist but cannot be created, or cannot be created for any other reason.*/
   EC_CREATE_FILE_FAILED = -10068,
   /**The input ImageData object contains invalid parameter(s).*/
   EC_IMGAE_DATA_INVALID = -10069,
   /**The size of the input image do not meet the requirements.*/
   EC_IMAGE_SIZE_NOT_MATCH = -10070,
   /**The pixel format of the input image do not meet the requirements.*/
   EC_IMAGE_PIXEL_FORMAT_NOT_MATCH = -10071,
   /**The section level result is irreplaceable.*/
   EC_SECTION_LEVEL_RESULT_IRREPLACEABLE = -10072,
   /**The axis definition is incorrect.*/
   EC_AXIS_DEFINITION_INCORRECT = -10073,
   /**The result is not replaceable due to type mismatch*/
   EC_RESULT_TYPE_MISMATCH_IRREPLACEABLE = -10074,
   /**Failed to load the PDF library.*/
   EC_PDF_LIBRARY_LOAD_FAILED = -10075,
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
   /** Instance count is over limit. */
   EC_INSTANCE_COUNT_OVER_LIMIT = -20008,
   /** Trial License */
   EC_TRIAL_LICENSE = -20010,
   /**Online license validation failed due to network issues. Using cached license information for validation*/
   EC_LICENSE_CACHE_USED = -20012,
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
   /**There is a conflict in the layout of TextLineGroup. */
   EC_TEXT_LINE_GROUP_LAYOUT_CONFLICT = -40101,
   /**There is a conflict in the regex of TextLineGroup. */
   EC_TEXT_LINE_GROUP_REGEX_CONFLICT = -40102,
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
public enum EnumErrorCode
{
    /**Successful. */
    EC_OK = 0,
    /** -10000~-19999: Common error code. */
    /**Unknown error. */
    EC_UNKNOWN = -10000,
    /**Not enough memory to perform the operation. */
    EC_NO_MEMORY = -10001,
    /**Null pointer */
    EC_NULL_POINTER = -10002,
    /**License invalid*/
    EC_LICENSE_INVALID = -10003,
    /**License expired*/
    EC_LICENSE_EXPIRED = -10004,
    /**File not found*/
    EC_FILE_NOT_FOUND = -10005,
    /**The file type is not supported. */
    EC_FILE_TYPE_NOT_SUPPORTED = -10006,
    /**The BPP (Bits Per Pixel) is not supported. */
    EC_BPP_NOT_SUPPORTED = -10007,
    /**The index is invalid.*/
    EC_INDEX_INVALID = -10008,
    /**The input region value parameter is invalid.*/
    EC_CUSTOM_REGION_INVALID = -10010,
    /**Failed to read the image. */
    EC_IMAGE_READ_FAILED = -10012,
    /**Failed to read the TIFF image. */
    EC_TIFF_READ_FAILED = -10013,
    /**The DIB (Device-Independent Bitmaps) buffer is invalid. */
    EC_DIB_BUFFER_INVALID = -10018,
    /**Failed to read the PDF image. */
    EC_PDF_READ_FAILED = -10021,
    /**The PDF DLL is missing. */
    EC_PDF_DLL_MISSING = -10022,
    /**The page number is invalid. */
    EC_PAGE_NUMBER_INVALID = -10023,
    /**The custom size is invalid. */
    EC_CUSTOM_SIZE_INVALID = -10024,
    /** timeout. */
    EC_TIMEOUT = -10026,
    /**Json parse failed*/
    EC_JSON_PARSE_FAILED = -10030,
    /**Json type invalid*/
    EC_JSON_TYPE_INVALID = -10031,
    /**Json key invalid*/
    EC_JSON_KEY_INVALID = -10032,
    /**Json value invalid*/
    EC_JSON_VALUE_INVALID = -10033,
    /**Json name key missing*/
    EC_JSON_NAME_KEY_MISSING = -10034,
    /**The value of the key "Name" is duplicated.*/
    EC_JSON_NAME_VALUE_DUPLICATED = -10035,
    /**Template name invalid*/
    EC_TEMPLATE_NAME_INVALID = -10036,
    /**The name reference is invalid.*/
    EC_JSON_NAME_REFERENCE_INVALID = -10037,
    /**Parameter value invalid*/
    EC_PARAMETER_VALUE_INVALID = -10038,
    /**The domain of your current site does not match the domain bound in the current product key.*/
    EC_DOMAIN_NOT_MATCH = -10039,
    /**The reserved info does not match the reserved info bound in the current product key.*/
    EC_RESERVED_INFO_NOT_MATCH = -10040,
    /**The license key does not match the license content.*/
    EC_LICENSE_KEY_NOT_MATCH = -10043,
    /**Failed to request the license content.*/
    EC_REQUEST_FAILED = -10044,
    /**Failed to init the license.*/
    EC_LICENSE_INIT_FAILED = -10045,
    /**Failed to set mode's argument.*/
    EC_SET_MODE_ARGUMENT_ERROR = -10051,
    /**The license content is invalid.*/
    EC_LICENSE_CONTENT_INVALID = -10052,
    /**The license key is invalid.*/
    EC_LICENSE_KEY_INVALID = -10053,
    /**The license key has no remaining quota.*/
    EC_LICENSE_DEVICE_RUNS_OUT = -10054,
    /**Failed to get mode's argument.*/
    EC_GET_MODE_ARGUMENT_ERROR = -10055,
    /**The Intermediate Result Types license is invalid.*/
    EC_IRT_LICENSE_INVALID = -10056,
    /**Failed to save file.*/
    EC_FILE_SAVE_FAILED = -10058,
    /**The stage type is invalid.*/
    EC_STAGE_TYPE_INVALID = -10059,
    /**The image orientation is invalid.*/
    EC_IMAGE_ORIENTATION_INVALID = -10060,
    /**Complex template can't be converted to simplified settings.*/
    EC_CONVERT_COMPLEX_TEMPLATE_ERROR = -10061,
    /**Reject function call while capturing in progress.*/
    EC_CALL_REJECTED_WHEN_CAPTURING = -10062,
    /**The input image source was not found.*/
    EC_NO_IMAGE_SOURCE = -10063,
    /**Failed to read directory.*/
    EC_READ_DIRECTORY_FAILED = -10064,
    /**[Name] Module not found.*/
    /**Name: */
    /**DynamsoftBarcodeReader*/
    /**DynamsoftLabelRecognizer*/
    /**DynamsoftDocumentNormalizer*/
    EC_MODULE_NOT_FOUND = -10065,
    /**The api does not support multi-page files. Please use FileFetcher instead.*/
    EC_MULTI_PAGES_NOT_SUPPORTED = -10066,
    /**The file already exists but overwriting is disabled.*/
    EC_FILE_ALREADY_EXISTS = -10067,
    /**The file path does not exist but cannot be created, or the file 
    cannot be created for any other reason.*/
    EC_CREATE_FILE_FAILED = -10068,
    /**The input ImageData object contains invalid parameter(s).*/
    EC_IMAGE_DATA_INVALID = -10069,
    /**The size of the input image does not meet the requirements.*/
    EC_IMAGE_SIZE_NOT_MATCH = -10070,
    /**The pixel format of the input image does not meet the requirements.*/
    EC_IMAGE_PIXEL_FORMAT_NOT_MATCH = -10071,
    /**The section level result is irreplaceable.*/
    EC_SECTION_LEVEL_RESULT_IRREPLACEABLE = -10072,
    /**The axis definition is incorrect.*/
    EC_AXIS_DEFINITION_INCORRECT = -10073,
    /**The result is not replaceable due to type mismatch.*/
    EC_RESULT_TYPE_MISMATCH_IRREPLACEABLE = -10074,
    /** -20000~-29999: DLS license error code. */
    /**No license.*/
    EC_NO_LICENSE = -20000,
    /**The Handshake Code is invalid.*/
    EC_HANDSHAKE_CODE_INVALID = -20001,
    /**Failed to read or write license buffer. */
    EC_LICENSE_BUFFER_FAILED = -20002,
    /**Failed to synchronize license info with license server. */
    EC_LICENSE_SYNC_FAILED = -20003,
    /**Device dose not match with buffer. */
    EC_DEVICE_NOT_MATCH = -20004,
    /**Failed to bind device. */
    EC_BIND_DEVICE_FAILED = -20005,
    /**License Client dll is missing.*/
    EC_LICENSE_CLIENT_DLL_MISSING = -20007,
    /**Instance count is over limit.*/
    EC_INSTANCE_COUNT_OVER_LIMIT = -20008,
    /**Interface InitLicense has to be called before creating any SDK objects.*/
    EC_LICENSE_INIT_SEQUENCE_FAILED = -20009,
    /**Trial License*/
    EC_TRIAL_LICENSE = -20010,
    /**The license is not valid for current version*/
    EC_LICENSE_VERSION_NOT_MATCH = -20011,
    /**Online license validation failed due to network issues. Using cached license information for validation*/
    EC_LICENSE_CACHE_USED = -20012,
    /**Failed to reach License Server.*/
    EC_FAILED_TO_REACH_DLS = -20200,
    /**-30000~-39999: DBR error code*/
    /**The barcode format is invalid.*/
    EC_BARCODE_FORMAT_INVALID = -30009,
    /**The QR Code license is invalid.*/
    EC_QR_LICENSE_INVALID = -30016,
    /**The 1D Barcode license is invalid.*/
    EC_1D_LICENSE_INVALID = -30017,
    /**The PDF417 license is invalid.*/
    EC_PDF417_LICENSE_INVALID = -30019,
    /**The DATAMATRIX license is invalid. */
    EC_DATAMATRIX_LICENSE_INVALID = -30020,
    /**The custom module size is invalid. */
    EC_CUSTOM_MODULESIZE_INVALID = -30025,
    /**The AZTEC license is invalid.*/
    EC_AZTEC_LICENSE_INVALID = -30041,
    /**The Patchcode license is invalid.*/
    EC_PATCHCODE_LICENSE_INVALID = -30046,
    /**The Postal code license is invalid.*/
    EC_POSTALCODE_LICENSE_INVALID = -30047,
    /**The DPM license is invalid.*/
    EC_DPM_LICENSE_INVALID = -30048,
    /**The frame decoding thread already exists.*/
    EC_FRAME_DECODING_THREAD_EXISTS = -30049,
    /**Failed to stop the frame decoding thread.*/
    EC_STOP_DECODING_THREAD_FAILED = -30050,
    /**The Maxicode license is invalid.*/
    EC_MAXICODE_LICENSE_INVALID = -30057,
    /**The GS1 Databar license is invalid.*/
    EC_GS1_DATABAR_LICENSE_INVALID = -30058,
    /**The GS1 Composite code license is invalid.*/
    EC_GS1_COMPOSITE_LICENSE_INVALID = -30059,
    /**The DotCode license is invalid.*/
    EC_DOTCODE_LICENSE_INVALID = -30061,
    /**The Pharmacode license is invalid.*/
    EC_PHARMACODE_LICENSE_INVALID = -30062,
    /**-40000~-49999: DLR error code*/
    /**Character Model file is not found*/
    EC_CHARACTER_MODEL_FILE_NOT_FOUND = -40100,
    /**There is a conflict in the layout of TextLineGroup. */
    EC_TEXT_LINE_GROUP_LAYOUT_CONFLICT = -40101,
    /**There is a conflict in the regex of TextLineGroup. */
    EC_TEXT_LINE_GROUP_REGEX_CONFLICT = -40102,
    /**-50000~-59999: DDN error code*/
    /*The quardrilateral is invalid*/
    EC_QUADRILATERAL_INVALID = -50057,
    /**-60000~-69999: DCE error code*/
    /**-70000~-79999: Panorama error code*/
    /**The panorama license is invalid.*/
    EC_PANORAMA_LICENSE_INVALID = -70060,
    /**-80000~-89999: Reserved error code*/
    /**-90000~-99999: DCP error code*/
    /*The resource path does not exist.*/
    EC_RESOURCE_PATH_NOT_EXIST = -90001,
    /*Failed to load resource.*/
    EC_RESOURCE_LOAD_FAILED = -90002,
    /*The code specification is not found.*/
    EC_CODE_SPECIFICATION_NOT_FOUND = -90003,
    /*The full code string is empty.*/
    EC_FULL_CODE_EMPTY = -90004,
    /*Failed to preprocess the full code string.*/
    EC_FULL_CODE_PREPROCESS_FAILED = -90005,
    /*The license for parsing South Africa Driver License is invalid.*/
    EC_ZA_DL_LICENSE_INVALID = -90006,
    /*The license for parsing North America DL/ID is invalid.*/
    EC_AAMVA_DL_ID_LICENSE_INVALID = -90007,
    /*The license for parsing Aadhaar is invalid.*/
    EC_AADHAAR_LICENSE_INVALID = -90008,
    /*The license for parsing Machine Readable Travel Documents is invalid.*/
    EC_MRTD_LICENSE_INVALID = -90009,
    /*The license for parsing Vehicle Identification Number is invalid.*/
    EC_VIN_LICENSE_INVALID = -90010,
    /*The license for parsing customized code type is invalid.*/
    EC_CUSTOMIZED_CODE_TYPE_LICENSE_INVALID = -90011
}
```
