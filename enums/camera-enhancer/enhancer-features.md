---
layout: default-layout
title: EnhancerFeatures - Dynamsoft Camera Enhancer Enumerations
description: The enumeration EnhancerFeatures of Dynamsoft Camera Enhancer describes the features of camera enhancer.
keywords:  Camera enhancer features
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: EnhancerFeatures
---

# EnhancerFeatures

Enumeration `EnhancerFeatures` indicates the advanced features of Dynamsoft Camera Enhancer.

- `Frame Filter`: The frame sharpness filter feature of DCE. By enabling this feature, the low-quality frame will be recognized and discarded automatically.
- `Sensor Control`: The sensor filter feature of DCE. By enabling this feature, the frames will be discarded automatically while the device is shaking.
- `Enhanced Focus`: The enhanced focus feature. DCE will support the camera in triggering auto-focus.
- `Fast Mode`: The fast mode of DCE. By enabling the fast mode, the frames will be cropped to speed up the following processing.
- `Auto Zoom`: The auto-zoom feature of DCE. By enabling this feature, the camera will automatically zoom in to the interest area.
- `Smart Torch`: Add a smart torch on the UI. The torch will be hided when the environment brightness is high and displayed when the brightness is low.

<div class="sample-code-prefix template2"></div>
   >- JavaScript
   >- Android
   >- Objective-C
   >- Swift
   >
>
```javascript
```
>
```java
@Retention(RetentionPolicy.CLASS)
public @interface EnumEnhancedFeatures {
   //Enable the Frame filter feature of DCE
   public static final int EF_FRAME_FILTER = 0x01;
   //Enable the sensor control feature of DCE
   public static final int EF_SENSOR_CONTROL = 0x02;
   //Enable the camera focus features of DCE
   public static final int EF_ENHANCED_FOCUS = 0x04;
   //Enable the autozoom feature
   public static final int EF_AUTO_ZOOM = 0x10;
   //Enable the smart torch button
   public static final int EF_SMART_TORCH = 0x20;
   // Enable all.
   public static final int EF_ALL = 0x3F;
}
```
>
```objc
typedef NS_ENUM(NSInteger, DSEnhancedFeatures)
{
   /**
    * Enable frame filter feature of the camera enhancer to make a filter out the low-quality frames.
    */
   EnhancedFeatureFrameFilter = 0X01,
   /**
    * Enable sensor control to filter out all the frames when the device is shaking.
    */
   EnhancedFeatureSensorControl = 0X02,
   /**
    * Enhanced focus helps low-end devices on focusing.
    */
   EnhancedFeatureEnhancedFocus = 0X04,
   /**
    * Enable the camera zoom-in automatically when barcode is far away.
    */
   EnhancedFeatureAutoZoom = 0X10,
   /**
    * Display a torch button when the environment light is low.
    */
   EnhancedFeatureSmartTorch = 0X20,
   /**
    * Enable all the enhanced features.
    */
   EnhancedFeatureAll = 0X3F
};
```
>
```swift
public enum EnhancedFeatures : Int{
   /**
    * Enable frame filter feature of the camera enhancer to make a filter out the low-quality frames.
    */
   frameFilter = 0X01
   /**
    * Enable sensor control to filter out all the frames when the device is shaking.
    */
   sensorControl = 0X02
   /**
    * Enhanced focus helps low-end devices on focusing.
    */
   enhancedFocus = 0X04
   /**
    * Enable the camera zoom-in automatically when barcode is far away.
    */
   autoZoom = 0X10
   /**
    * Display a torch button when the environment light is low.
    */
   smartTorch = 0X20
   /**
    * Enable all the enhanced features.
    */
   all = 0X3F
}
```
