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

`ErrorCode` describes the error code that can be output by the library.

<div class="sample-code-prefix template2"></div>
   >- JavaScript
   >- Android
   >- Objective-C
   >- Swift
   >- C++
   >
>
```javascript
enum EnumErrorCode
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
   EC_FILETYPE_NOT_SUPPORTED = -10006,
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
   EC_DOMAIN_NOT_MATCHED = -10039,
   /**The reserved info does not match the reserved info bound in the current product key.*/
   EC_RESERVEDINFO_NOT_MATCHED = -10040,
   /**The license key does not match the license content.*/
   EC_LICENSEKEY_NOT_MATCHED = -10043,
   /**Failed to request the license content.*/
   EC_REQUESTED_FAILED = -10044,
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
   /**Complex tempalte can't be converted to simplified settings.*/
   EC_CONVERT_COMPLEX_TEMPLATE_ERROR = -10061,
   /**Can't update settings at runtime.*/
   EC_UPDATE_SETTINGS_AT_RUNTIME_FAILED = -10062,
   /**The input image source was not found.*/
   EC_NO_IMAGE_SOURCE = -10063,
   /**Failed to read directory.*/
   EC_READ_DIRECTORY_FAILED = -10064,
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
   /**Interface InitLicenseFromDLS can not be used together with other license initiation interfaces. */
   EC_LICENSE_INTERFACE_CONFLICT = -20006,
   /**License Client dll is missing.*/
   EC_LICENSE_CLIENT_DLL_MISSING = -20007,
   /**Instance count is over limit.*/
   EC_INSTANCE_COUNT_OVER_LIMIT = -20008,
   /**Interface InitLicenseFromDLS has to be called before creating any SDK objects.*/
   EC_LICENSE_INIT_SEQUENCE_FAILED = -20009,
   /**Trial License*/
   EC_TRIAL_LICENSE = -20010,
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
   /**-50000~-59999: DDN error code*/
   /**No content has been detected.*/
   EC_CONTENT_NOT_FOUND = -50056,
   /*The quardrilateral is invalid*/
   EC_QUADRILATERAL_INVALID = -50057,
   /**-60000~-69999: DCE error code*/
   EC_CAMERA_MODULE_NOT_EXIST = -60003,
   EC_CAMERA_ID_NOT_EXIST = -60006,
   EC_NO_SENSOR = -60045,
   /**-70000~-79999: Panorama error code*/
   /**The panorama license is invalid.*/
   EC_PANORAMA_LICENSE_INVALID = -70060,
   /**-80000~-89999: Reserved error code*/
   /**-90000~-99999: DCP error code*/
   EC_RESOURCE_PATH_NOT_EXIST = -90001,
   /*Failed to load resource*/
   EC_RESOURCE_LOAD_FAILED = -90002,
   /*The code specification is not found*/
   EC_CODE_SPECIFICATION_NOT_FOUND = -90003,
   /*The full code string is empty*/
   EC_FULL_CODE_EMPTY = -90004,
   /*Failed to preprocess the full code string*/
   EC_FULL_CODE_PREPROCESS_FAILED = -90005,
   /* The license for parsing South Africa Driver License is invalid*/
   EC_ZA_DL_LICENSE_INVALID = -90006,
   /* The license for parsing North America DL/ID is invalid*/
   EC_AAMVA_DL_ID_LICENSE_INVALID = -90007,
   /* The license for parsing Aadhaar is invalid*/
   EC_AADHAAR_LICENSE_INVALID = -90008,
   /* The license for parsing Machine Readable Travel Documents is invalid*/
   EC_MRTD_LICENSE_INVALID = -90009,
   /* The license for parsing Vehicle Identification Number is invalid*/
   EC_VIN_LICENSE_INVALID = -90010,
   /* The license for parsing customized code type is invalid*/
   EC_CUSTOMIZED_CODE_TYPE_LICENSE_INVALID = -90011,
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
typedef NS_ERROR_ENUM(DSErrorDomain, DSErrorCode) {
   /**Successful. */
   DSErrorCodeOK                               = 0,
   /**Unknown error. */
   DSErrorCodeUnknown                          = -10000,
   /**Not enough memory to perform the operation. */
   DSErrorCodeNoMemory                         = -10001,
   /**Null pointer */
   DSErrorCodeNullPointer                      = -10002,
   /**License invalid*/
   DSErrorCodeLicenseInvalid                   = -10003,
   /**License expired*/
   DSErrorCodeLicenseExpired                   = -10004,
   /**File not found*/
   DSErrorCodeFileNotFound                     = -10005,
   /**The file type is not supported. */
   DSErrorCodeFiletypeNotSupported             = -10006,
   /**The BPP (Bits Per Pixel) is not supported. */
   DSErrorCodeBPPNotSupported                  = -10007,
   /**Failed to read the image. */
   DSErrorCodeImageReadFailed                  = -10012,
   /**Failed to read the TIFF image. */
   DSErrorCodeTiffReadFailed                   = -10013,
   /**The DIB (Device-Independent Bitmaps) buffer is invalid. */
   DSErrorCodeDIBBufferInvalid                 = -10018,
   /**Failed to read the PDF image. */
   DSErrorCodePdfReadFailed                    = -10021,
   /**The PDF DLL is missing. */
   DSErrorCodePdfDllMissing                    = -10022,
   /**The page number is invalid. */
   DSErrorCodePageNumberInvalid                = -10023,
   /**The custom size is invalid. */
   DSErrorCodeCustomSizeInvalid                = -10024,
   /** timeout. */
   DSErrorCodeTimeout                          = -10026,
   /**Json parse failed*/
   DSErrorCodeJsonParseFailed                  = -10030,
   /**Json type invalid*/
   DSErrorCodeJsonTypeInvalid                  = -10031,
   /**Json key invalid*/
   DSErrorCodeJsonKeyInvalid                   = -10032,
   /**Json value invalid*/
   DSErrorCodeJsonValueInvalid                 = -10033,
   /**Json name key missing*/
   DSErrorCodeJsonNameKeyMissing               = -10034,
   /**The value of the key "Name" is duplicated.*/
   DSErrorCodeJsonNameValueDuplicated          = -10035,
   /**Template name invalid*/
   DSErrorCodeTemplateNameInvalid              = -10036,
   /**The name reference is invalid.*/
   DSErrorCodeJsonNameReferenceInvalid         = -10037,
   /**Parameter value invalid*/
   DSErrorCodeParameterValueInvalid            = -10038,
   /**The domain of your current site does not match the domain bound in the current product key.*/
   DSErrorCodeDomainNotMatch                   = -10039,
   /**The reserved info does not match the reserved info bound in the current product key.*/
   DSErrorCodeReservedInfoNotMatch             = -10040,
   /**The license key does not match the license content.*/
   DSErrorCodeLicenseKeyNotMatch               = -10043,
   /**Failed to request the license content.*/
   DSErrorCodeRequestFailed                    = -10044,
   /**Failed to init the license.*/
   DSErrorCodeLicenseInitFailed                = -10045,
   /**Failed to set mode's argument.*/
   DSErrorCodeSetModeArgumentError             = -10051,
   /**The license content is invalid.*/
   DSErrorCodeLicenseContentInvalid            = -10052,
   /**The license key is invalid.*/
   DSErrorCodeLicenseKeyInvalid                = -10053,
   /**The license key has no remaining quota.*/
   DSErrorCodeLicenseDeviceRunsOut             = -10054,
   /**Failed to get mode's argument.*/
   DSErrorCodeGetModeArgumentError             = -10055,
   /**The Intermediate Result Types license is invalid.*/
   DSErrorCodeIrtLicenseInvalid                = -10056,
   /**Failed to save file.*/
   DSErrorCodeFileSaveFailed                   = -10058,
   /**The stage type is invalid.*/
   DSErrorCodeStageTypeInvalid                 = -10059,
   /**The image orientation is invalid.*/
   DSErrorCodeImageOrientationInvalid          = -10060,
   /**Failed to convert complex tempalte to simplified settings.*/
   DSErrorCodeConvertComplexTemplateError      = -10061,
   /**Reject function call while capturing in progress.*/
   DSErrorCodeCallRejectedWhenCapturing        = -10062,
   /**The input image source was not found.*/
   DSErrorCodeNoImageSource                    = -10063,
   /**Failed to read directory.*/
   DSErrorCodeReadDirectoryFailed              = -10064,
   /**[Name] Module not found.*/
   /**Name : */
   /**DynamsoftBarcodeReader*/
   /**DynamsoftLabelRecognizer*/
   /**DynamsoftDocumentNormalizer*/
   DSErrorCodeModuleNotFound                   = -10065,
   /**No license.*/
   DSErrorCodeNoLicense                        = -20000,
   /**The handshake code is invalid. */
   DSErrorCodeHandshakeCodeInvalid             = -20001,
   /**Failed to read or write license cache. */
   DSErrorCodeLicenseBufferFailed              = -20002,
   /**Falied to synchronize license info wirh license tracking server. */
   DSErrorCodeLicenseSyncFailed                = -20003,
   /**Device does not match with license buffer. */
   DSErrorCodeDeviceNotMatch                   = -20004,
   /**Falied to bind device. */
   DSErrorCodeBindDeviceFailed                 = -20005,
   /**Install.*/
   DSErrorCodeInstanceCountOverLimit           = -20008,
   /**Trial License*/
   DSErrorCodeTrialLicense                     = -20010,
   /**The license is not valid for current version*/
   DSErrorCodeLicenseVersionNotMatch           = -20011,
   /**Failed to reach License Tracking Server.*/
   DSErrorCodeFailedToReachDLS                 = -20200
   /** -30000~-39999: DBR error code. */
   /** The barcode format is invalid. */
   DSErrorCodeBarcodeFormatInvalid             = -30009,
   /** The QR Code license is invalid. */
   DSErrorCodeQRLicenseInvalid                 = -30016,
   /** The 1D Barcode license is invalid. */
   DSErrorCode1DLicenseInvalid                 = -30017,
   /** The PDF417 license is invalid. */
   DSErrorCodePDF417LicenseInvalid             = -30019,
   /** The DATAMATRIX license is invalid. */
   DSErrorCodeDATAMATRIXLicenseInvalid         = -30020,
   /** The custom module size is invalid. */
   DSErrorCodeCustomModuleSizeInvalid          = -30025,
   /** The AZTEC license is invalid. */
   DSErrorCodeAztecLicenseInvalid              = -30041,
   /** The Patchcode license is invalid. */
   DSErrorCodePatchCodeLicenseInvalid          = -30046,
   /** The Postal code license is invalid. */
   DSErrorCodePostalCodeLicenseInvalid         = -30047,
   /** The DPM license is invalid. */
   DSErrorCodeDPMLicenseInvalid                = -30048,
   /** The frame decoding thread already exists. */
   DSErrorCodeFrameDecodingThreadExists        = -30049,
   /** Failed to stop the frame decoding thread. */
   DSErrorCodeStopDecodingThreadFailed         = -30050,
   /** The Maxicode license is invalid. */
   DSErrorCodeMaxiCodeLicenseInvalid           = -30057,
   /** The GS1 Databar license is invalid. */
   DSErrorCodeGS1DatabarLicenseInvalid         = -30058,
   /** The GS1 Composite code license is invalid. */
   DSErrorCodeGS1CompositeLicenseInvalid       = -30059,
   /** The DotCode license is invalid. */
   DSErrorCodeDotCodeLicenseInvalid            = -30061,
   /** The Pharmacode license is invalid. */
   DSErrorCodePharmaCodeLicenseInvalid         = -30062,
   /** -40000~-49999: DLR error code */
   /** Character Model file is not found. */
   DSErrorCodeCharacterModelFileNotFound       = -40100,
   /** -50000~-59999: DDN error code. */
   /**No content has been detected. */
   DSErrorCodeContentNotFound                  = -50056,
   /*The quardrilateral is invalid. */
   DSErrorCodeQuardrilateralInvalid            = -50057,
   /** -60000~-69999: DCE error code. */
   DSErrorCodeCameraModelNotExist              = -60003,
   DSErrorCodeCameraIDNotExist                 = -60006,
   DSErrorCodeNoSensor                         = -60045,
   /**-70000~-79999: Panorama error code. */
   /**The panorama license is invalid. */
   DSErrorCodePanoramaLicenseInvalid           = -70060,
   /** -80000~-89999: Reserved error code. */
   /**-90000~-99999: DCP error code. */
   /** The resource path is not exist. */
   DSErrorCodeResourcePathNotExist             = -90001,
   /** Failed to load resource. */
   DSErrorCodeResourceLoadFailed               = -90002,
   /** The code specification is not found. */
   DSErrorCodeCodeSpecificationNotFound        = -90003,
   /** The full code string is empty. */
   DSErrorCodeFullCodeEmpty                    = -90004,
   /** Failed to preprocess the full code string */
   DSErrorCodeFullCodePreprocessFailed         = -90005,
   /** The license for parsing South Africa Driver License is invalid. */
   DSErrorCodeZADLLicenseInvalid               = -90006,
   /** The license for parsing North America DL/ID is invalid. */
   DSErrorCodeAAMVADLIDLicenseInvalid          = -90007,
   /** The license for parsing Aadhaar is invalid. */
   DSErrorCodeAADHAARLicenseInvalid            = -90008,
   /** The license for parsing Machine Readable Travel Documents is invalid. */
   DSErrorCodeMRTDLicenseInvalid               = -90009,
   /** The license for parsing Vehicle Identification Number is invalid. */
   DSErrorCodeVINLicenseInvalid                = -90010,
   /** The license for parsing customized code type is invalid. */
   DSErrorCodeCustomizedCodeTypeLicenseInvalid = -90011,
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
