---
layout: default-layout
title: License Activation - Dynamsoft SDKs
keywords: license
breadcrumbText: License Activation
description: License Activation Page
---

# License Activation

## Get a License

### Trial License

To test Dynamsoft SDKs, request a 30-day trial license through the [Request a Trial License](https://www.dynamsoft.com/customer/license/trialLicense/?utm_source=dcvCoreDocs&product=dcv&package=core) link.

### Full License

For using Dynamsoft SDKs in production, [Contact us](https://www.dynamsoft.com/company/contact/?utm_source=dcvCoreDocs&product=dcv&package=core) to purchase a full license.

## Activate the License

The following code snippets demonstrate how to activate a license.

<div class="sample-code-prefix template2"></div>
>- JavaScript
>- C++
>- Java-Android
>- Objective-C
>- Swift
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