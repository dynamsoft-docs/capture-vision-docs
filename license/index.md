---
layout: default-layout
title: License Initialization - Dynamsoft SDKs
keywords: license
description: License Initialization Page
---

# License Initialization

This guide outlines the steps required to initialize a license for the following Dynamsoft products:

* Dynamsoft Barcode Reader
* Dynamsoft Capture Vision
* MRZ Scanner

## Obtaining a License

### Trial License

To evaluate Dynamsoft SDKs, you can request a 30-day trial license by clicking [Request a Trial License](https://www.dynamsoft.com/customer/license/trialLicense/?utm_source=docs&product=dcv).

### Full License

For production use, please [contact our sales team](https://www.dynamsoft.com/company/contact/?utm_source=docs&product=dcv) to purchase a full license.

## Activating the License

The following code snippets provide guidance on how to activate the license for your application.

<div class="sample-code-prefix template2"></div>
>- JavaScript
>- C++
>- Android
>- Objective-C
>- Swift
>- C#
>- Python
>
```js
Dynamsoft.License.LicenseManager.initLicense("--Enter Your License Key Here--");
```
>
```cpp
int errorCode = 0;
char szErrorMsg[256];
errorCode = CLicenseManager::InitLicense("--Enter Your License Key Here--", szErrorMsg, 256);
if (errorCode != DM_OK)
   cout << szErrorMsg << endl;
```
> 
```java
LicenseManager.initLicense("--Enter Your License Key Here--", MainActivity.this, new LicenseVerificationListener() {
   @Override
   public void licenseVerificationCallback(boolean isSuccess, CoreException error) {
          if(!isSuccess){
             error.printStackTrace();
          }
   }
});
```
>
```objc
[DynamsoftLicenseManager initLicense:@"--Enter Your License Key Here--" verificationDelegate: self];
- (void)licenseVerificationCallback:(BOOL)isSuccess error:(NSError *)error{
   // Add your code to execute when license verification call back is handled.
}
```
>
```swift
DynamsoftLicenseManager.initLicense("--Enter Your License Key Here--", verificationDelegate: self)
func licenseVerificationCallback(_ isSuccess: Bool, error: Error?) {
   // Add your code to execute when license verification call back is handled.
}
```
>
```csharp
int errorCode = 0;
string errorMsg;
errorCode = LicenseManager.InitLicense("--Enter Your License Key Here--", out errorMsg);
if (errorCode != (int)EnumErrorCode.EC_OK && errorCode != (int)EnumErrorCode.EC_LICENSE_CACHE_USED)
{
    Console.WriteLine("License initialization error: " + errorMsg);
}
else
{
    CaptureVisionRouter cvr = new CaptureVisionRouter();
    // add code for further process
}
```
>
```python
error_code, error_msg = LicenseManager.init_license("--Enter Your License Key Here--")
if error_code != EnumErrorCode.EC_OK.value and error_code != EnumErrorCode.EC_LICENSE_CACHE_USED.value:
    print("License initialization error: " + error_msg)
else:
    CaptureVisionRouter cvr = new CaptureVisionRouter()
    # add code for further process
```
