---
layout: default-layout
title: License Activation - Dynamsoft SDKs
keywords: license
breadcrumbText: License Activation
description: License Activation Page
---

# License Activation

## Get a trial key

To test Dynamsoft SDKs, you can request a 30-day trial license via the [Request a Trial License](https://www.dynamsoft.com/customer/license/trialLicense/) link.

## Get a full license

- [Contact us](https://www.dynamsoft.com/company/contact/) to purchase a full license.

## Activate the license

The following code snippets demonstrate how to activate a license.

<div class="sample-code-prefix"></div>
>- JavaScript
>- C++
>- Java-Android
>- Objective-C
>- Swift
>
>
1. 
```js
Dynamsoft.License.LicenseManager.initLicense("--Enter Your License Key Here--");
```
2.
```cpp
int errorCode = 0;
char szErrorMsg[256];
errorCode = CLicenseManager::InitLicense("--Enter Your License Key Here--", szErrorMsg, 256);
if (errorCode != DM_OK)
   cout << szErrorMsg << endl;
```
3. 
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
4. 
```objc
[DynamsoftLicenseManager initLicense:@"--Enter Your License Key Here--" verificationDelegate: self];
- (void)licenseVerificationCallback:(BOOL)isSuccess error:(NSError *)error{
   // Add your code to execute when license verification call back is handled.
}
```
5. 
```swift
DynamsoftLicenseManager.initLicense("--Enter Your License Key Here--", verificationDelegate: self)
func licenseVerificationCallback(_ isSuccess: Bool, error: Error?) {
   // Add your code to execute when license verification call back is handled.
}
```