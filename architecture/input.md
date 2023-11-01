---
layout: default-layout
title: Standard Input - Dynamsoft Capture Vision Architecture
description: This article is about the standard input in the Dynamsoft Capture Vision architecture.
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: false
permalink: /architecture/input.html
---

> *Go to [DCV Architecture](index.md)*

# Input

![DCV Architecture](assets/dcv-architecture-input.png)

In the Dynamsoft Capture Vision (DCV) architecture, "input" is what supplies the images to be processed, and we usually call it "the image source".

An image source refers to an object that has implemented the [Image Source Adapter (ISA)](#image-source-adapter) interface.

## Image Source Adapter

"Image Source Adapter" (ISA) is the interface that plugs an image source into a DCV application. The interface is designed to have the following features:

1. Return an image when requested by [Capture Vision Router (CVR)](index.md#capture-vision-router)
2. Maintain an image buffer to allow instant access of images (save the time it takes to open image files)

### Return an image when requested

This is the design purpose for an image source. To make it easy to use, ISA requires the following methods:

1. A method to return how many images are available. For example, `getImageCount()`
2. A method to check whether a specific image is available. For example, `hasImage()`
3. A method to set the order in which images are returned. For example, `setNextImageToReturn()`
4. A method to actually return an image. For example, `getImage()`

### Maintain an image buffer

This is to facilitate the returning of images by building up a buffer area. ISA requires the following methods to achieve it:

1. A method to add images. For example, `addImageToBuffer()`
2. Methods to control the buffer size. For example, `setMaxImageCount()` and `getMaxImageCount()`
3. Methods to control when to build the buffer. For example, `startFetching()` and `stopFetching()`
4. Methods to handle buffer overflow. For example, `setBufferOverflowProtectionMode()` and `getBufferOverflowProtectionMode()`
5. Other utility methods like `isBufferEmpty()` and `hasNextImageToFetch()`

## ISA Implementation

An image source is usually required when creating a DCV application. In most cases, developers can directly use one of the following ready-made implementations in their application:

### Dynamsoft Camera Enhancer

Dynamsoft Camera Enhancer (DCE) is available on Web and Mobile platforms. It enables the users to do the following:

1. Control cameras
2. Acquire image frames from a live video stream
3. Provide basic user interaction

As it has implemented the ISA interface, we can directly use it as an image source. For example:

<div class="sample-code-prefix template2"></div>
   >- JavaScript
   >- Android
   >- Objective-C
   >- Swift
   >
>
```javascript
let captureVisionRouter = Dynamsoft.CVR.CaptureVisionRouter.createInstance();
let cameraEnhancer = Dynamsoft.DCE.CameraEnhancer.createInstance();
captureVisionRouter.setInput(cameraEnhancer);
```
>
```java
CaptureVisionRouter router = new CaptureVisionRouter();
CameraView cameraView = findViewById(R.id.dce_camera_view);
CameraEnhancer dce = new CameraEnhancer(cameraView, activity);
router.setInput(dce);
```
>
```objc
@property(nonatomic, strong) DSCaptureVisionRouter *cvr;
@property(nonatomic, strong) DSCameraEnhancer *dce;
@property(nonatomic, strong) DSCameraView *dceView;
-(void)configurationDCV{
   _dceView = [DSCameraView cameraWithFrame:self.view.bounds];
   [self.view addSubview:_dceView];
   _dce = [[DSCameraEnhancer alloc] initWithView:_dceView];
   _cvr = [[DSCaptureVisionRouter alloc] init];
   [_cvr setInput:_dce];
}
```
>
```swift
var dce:CameraEnhancer!
var dceView:CameraView!
var cvr:CaptureVisionRouter!
func configurationDCV(){
   dceView = CameraView.init(frame: self.view.bounds)
   self.view.addSubview(dceView)
   dce = CameraEnhancer.init(view: dceView)
   cvr = CaptureVisionRouter.init()
   cvr.setInput(dce)
}
```

### Directory Fetcher

Directory Fetcher is available on Mobile and Desktop/Server Platforms. It enables users to simulate a directory containing images as an image source. For example:

<div class="sample-code-prefix template2"></div>
   >- Android
   >- Objective-C
   >- Swift
   >- C++
   >
>
```java
// Create a new instance of CaptureVisionRouter
CaptureVisionRouter router = new CaptureVisionRouter();
// Create a new instance of DirectoryFetcher
DirectoryFetcher fetcher = new DirectoryFetcher();
// Config the fetcher
fetcher.setImageFetchInterval(1000);
fetcher.setDirectory("/PATH/TO/DIRECTORY", "*.JPG", true);
// Set the fetcher as the input source
router.SetInput(fetcher);
// Start the image capture process
// ...
```
>
```objc
// Create a new instance of CaptureVisionRouter
DSCaptureVisionRouter* router = [[DSCaptureVisionRouter alloc] init];
// Create a new instance of DirectoryFetcher
DSDirectoryFetcher* fetcher = [[DSDirectoryFetcher alloc] init];
// Config the fetcher
[fetcher setImageFetchInterval:1000];
[fetcher setDirectory:@"/PATH/TO/DIRECTORY" filter:@"*.JPG" recursive:YES];
// Set the fetcher as the input source
[router setInput:fetcher];
// Start the image capture process
// ...
```
>
```swift
// Create a new instance of CaptureVisionRouter
var router = CaptureVisionRouter.init()
// Create a new instance of DirectoryFetcher
var fetcher = DirectoryFetcher.init()
// Config the fetcher
fetcher.setImageFetchInterval(1000)
fetcher.setDirectory("/PATH/TO/DIRECTORY", filter:"*.jpg", recursive:true)
// Set the fetcher as the input source
router.setInput(fetcher)
// Start the image capture process
// ...
```
>
```cpp
// Create a new instance of CCaptureVisionRouter
CCaptureVisionRouter* router = new CCaptureVisionRouter;
// Create a new instance of CDirectoryFetcher
CDirectoryFetcher *fetcher = new CDirectoryFetcher;
// Config the fetcher
fetcher->SetImageFetchInterval(1000);
fetcher->SetDirectory("/PATH/TO/DIRECTORY", "*.JPG", true);
// Set the fetcher as the input source
router->SetInput(fetcher);
// Start the image capture process
// ...
```

### Custom Implementation

An ISA implementation requires more than ten methods, which is not easy to do. Therefore, Dynamsoft provides a base class to help developers build their own. Check out the definition of the class for more information:

<div class="sample-code-prefix template2"></div>
   >- JavaScript
   >- Android
   >- Objective-C
   >- Swift
   >- C++
   >
>
```javascript
abstract class ImageSourceAdapter {
    constructor() { };
    /**
     * User has to implement this method themselves.
     */
    abstract hasNextImageToFetch: () => boolean;
    /**
     * Add images (of the type DSImageData) to the buffer.
     * This method will check if _isfetchingStarted is true. If not, it will refuse to add the image to buffer
     */
    addImageToBuffer: (image: Core.BasicStructures.DSImageData) => void;
    /**
     * Returns a buffered image.
     * @param removeFromBuffer Whether ISA should remove the image from Buffer after it is returned. `true` by default
     */
    getImage: (removeFromBuffer?: boolean) => Promise<Core.BasicStructures.DSImageData>;
    // Set _isfetchingStarted to true 
    startFetching: () => void;
    // Set _isfetchingStarted to false
    stopFetching: () => void;
    /**
     * This method can set the processing priority of an image.
     */
    setNextImageToReturn: (imageId: number, keepInBuffer?: boolean) => void;
    hasImage: (imageId: number) => boolean;
    /**
     * Sets how many images are allowed to be buffered.
     * @param recommendation: A class that implements the interface
     * should try to keep the buffer full if at all possible.*/
    setMaxImageCount: (count: number) => void;
    /**
     * Returns how many images can be buffered. 
     */
    getMaxImageCount: () => number;
    /**
     * Returns the actual count of buffered images. 
     */
    getImageCount: () => number;
    /**
     * Sets a mode that determines the action to take when there
     * is a new incoming image and the buffer is full.
     * @param mode specifies the mode
     * Allowed methods are defined in EnumBufferOverflowProtectionMode.
     */
    setBufferOverflowProtectionMode: (mode: Core.BasicStructures.EnumBufferOverflowProtectionMode) => void;
    getBufferOverflowProtectionMode: () => Core.BasicStructures.EnumBufferOverflowProtectionMode;
    /**
     * Determines whether the buffer is empty.
     */
    isBufferEmpty: () => boolean;
}
```
>
```java
public abstract class ImageSourceAdapter
{
    public abstract boolean hasNextImageToFetch();
    public void addImageToBuffer(ImageData image);
    /**
     * Returns a buffered image.
     * @param removeFromBuffer Whether ISA should remove the image from Buffer after it is returned.
     */
    public ImageData getImage();
    public void startFetching();
    public void stopFetching();
    /**
     * invoke setNextImageToReturn(imageId, true)
     */
    public boolean setNextImageToReturn(int imageId);
    public boolean setNextImageToReturn(int imageId, boolean keepInBuffer);
    public boolean hasImage(int imageId);
    /* Sets how many images are allowed to be buffered.
     * @recommendation A class that implements the interface
     * should try to keep the buffer full if at all possible.*/
    public void setMaximumImageCount(int count);
    /* Returns how many images can be buffered. */
    public int getMaximumImageCount();
    /* Sets a mode that determines the action to take when there
     * is a new incoming image and the buffer is full.
     * Allowed methods are defined in BufferOverflowProtectionMode.*/
    public void setBufferOverflowProtectionMode(BufferOverflowProtectionMode mode);
    public BufferOverflowProtectionMode getBufferOverflowProtectionMode();
    /* Returns the actual count of buffered images. */
    public int getImageCount();
    /** Determines whether the buffer is empty.*/
    public boolean isBufferEmpty();
    public void clearBuffer();
    public void setColourChannelUsageType(EnumColourChannelUsageType type);
    public EnumColourChannelUsageType getColourChannelUsageType();
}
```
>
```objc
@interface DSImageSourceAdapter
/** Defines whether there remains image from the source. If hasNextImageToFetch is false. */
@property (nonatomic, assign) BOOL hasNextImageToFetch;
/** Start fetching images from the source to the VideoBuffer of ImageSourceAdapter. */
- (void) startFetching;
/** Stop fetching images from the source to the VideoBuffer of ImageSourceAdapter. */
- (void) stopFetching;
/**
 * Get an image from the VideoBuffer. Dynamsoft Capture Vision will trigger this method to obtain new image.
 * 
 * @param [in] removeFromBuffer Whether to remove the image from the VideoBuffer.
 * @return An object of DSImageData.
 *     If an image is set as the "next image" by method setNextImageToReturn, return that image.
 *     If no image is set as the "next image", return the latest image.
 */
- (DSImageData *_Nullable)getImage:(BOOL)removeFromBuffer;
/** The property defines the maximum capability of the VideoBuffer an image from the VideoBuffer. */
@property (nonatomic, assign) NSUInteger maxImageCount;
/** The property overflow protection mode of the VideoBuffer. You can either block the VideoBuffer or push out the oldest image and append a new one. */
@property (nonatomic, assign) DSBufferOverflowProtectionMode bufferOverflowProtectionMode;
/**
 * Specify the next image that is returned by method getImage.
 * 
 * @param [in] imageId The imageId of image you want to set as the "next image".
 * @param [in] keepInBuffer Set this value to true so that the "next image" is protected from being pushed out before is it returned by method getImage.
 * @return A BOOL value that indicates whether the specified image is successfully set as the "next image".
 */
- (BOOL) setNextImageToReturn(NSInteger)imageId keepInBuffer(BOOL)keepInBuffer;
/**
 * Check the availability of the specified image.
 * 
 * @param [in] imageId The imageId of image you want to check the availability.
 * @return A BOOL value that indicates whether the specified image is found in the video buffer.
 */
- (BOOL) hasImage(NSInteger)imageId;
/** The property defines current image count in the VideoBuffer. */
@property (nonatomic, assign) NSUInteger imageCount;
/** The read only property defines whether the VideoBuffer is empty. */
@property (nonatomic, assign, readonly, getter=isBufferEmpty) BOOL bufferEmpty;//
/**
 * Append an image to the buffer.
 * 
 * @param [in] image An DSImageData object.
 */
- (void) addImageToBuffer:(DSImageData*)image;
@end
```
>
```swift
class ImageSourceAdapter: NSObject{
   /** Defines whether there remains image from the source. If hasNextImageToFetch is false. */
   var hasNextImageToFetch: Bool {get set}
   /** Start fetching images from the source to the VideoBuffer of ImageSourceAdapter. */
   func startFetching()
   /** Stop fetching images from the source to the VideoBuffer of ImageSourceAdapter. */
   func stopFetching()
   /**
    * Get an image from the VideoBuffer. Dynamsoft Capture Vision will trigger this method to obtain new image.
    *
    * @param [in] removeFromBuffer Whether to remove the image from the VideoBuffer.
    * @return An object of DSImageData.
    *     If an image is set as the "next image" by method setNextImageToReturn, return that image.
    *     If no image is set as the "next image", return the latest image.
    */
   func getImage(_ removeFromBuffer: Bool) -> ImageData
   /** The property defines the maximum capability of the VideoBuffer an image from the VideoBuffer. */
   var maxImageCount: Int { get set }
   /** The property overflow protection mode of the VideoBuffer. You can either block the VideoBuffer or push out the oldest image and append a new one. */
   var bufferOverflowProtectionMode: BufferOverflowProtectionMode { get set }
   /**
    * Specify the next image that is returned by method getImage.
    *
    * @param [in] imageId The imageId of image you want to set as the "next image".
    * @param [in] keepInBuffer Set this value to true so that the "next image" is protected from being pushed out before is it returned by method getImage.
    * @return A BOOL value that indicates whether the specified image is successfully set as the "next image".
    */
   func setNextImageToReturn(_ imageId: Int, keepInBuffer: Bool) -> Bool
   /**
    * Check the availability of the specified image.
    *
    * @param [in] imageId The imageId of image you want to check the availability.
    * @return A BOOL value that indicates whether the specified image is found in the video buffer.
    */
   func hasImage(_ imageId: Int) -> Bool
   /** The property defines current image count in the VideoBuffer. */
   var imageCount: Int { get set }
   /** The read only property defines whether the VideoBuffer is empty. */
   var bufferEmpty: Bool { get(isBufferEmpty) set }
   /**
    * Append an image to the buffer.
    *
    * @param [in] image An DSImageData object.
    */
   func addImageToBuffer(_ image: ImageData)
}
```
>
```cpp
class DS_API CImageSourceAdapter
{
protected:
    CImageSourceAdapter();
    /**
     * Add images (of the type CImageData) to the buffer.
     * This method will check if the internal flag indicating whether the fetching is started is true. If not, it will refuse to add the image to buffer
     */
    void AddImageToBuffer(const CImageData* img, bool bClone = true);
public:
    virtual ~CImageSourceAdapter();
    /** Determines whether there are more images left to fetch.*/
    virtual bool HasNextImageToFetch() const = 0;
    /**
     * Maintains the internal flag indicating whether the fetching is started
     */
    virtual void StartFetching();
    virtual void StopFetching();
    /**
     * Returns a buffered image.
     */
    virtual CImageData* GetImage();
    /* Gets or Sets how many images are allowed to be buffered.
     * @recommendation A class that implements the interface
     * should try to keep the buffer full if at all possible.*/
    void SetMaxImageCount(int count);
    int GetMaxImageCount() const ;
    /* Gets or Sets a mode that determines the action to take when there
     * is a new incoming image and the buffer is full.
     * Allowed methods are defined in BufferOverflowProtectionMode.*/
    void SetBufferOverflowProtectionMode(BufferOverflowProtectionMode mode);
    BufferOverflowProtectionMode GetBufferOverflowProtectionMode() const;
    /* Determines whether the image is in the buffer or not. */
    bool HasImage(int imageId) const;
    /* Sets the Next Image To Return. */
    bool SetNextImageToReturn(int imageId, bool keepInBuffer = true);
    /* Returns the actual count of buffered images. */
    int GetImageCount() const;
    /* Determines whether the buffer is empty.*/
    bool IsBufferEmpty() const;
    /**
    * Sets the usage type of a color channel in images.
    */
    void SetColourChannelUsageType(ColourChannelUsageType type);
    /**
    * Gets the usage type of a color channel in images.
    *
    * @return Returns the usage type of a color channel in images.
    *
    */
    ColourChannelUsageType GetColourChannelUsageType()const;
    /**
    * Sets the error listener for the image source. This function allows you to set an error listener object that will receive notifications when errors occur during image source operations.
    * If an error occurs, the error infomation will be passed to the listener's OnErrorReceived method.
    * @param [in] listener A pointer to an instance of CImageSourceErrorListener or its derived class, which will handle error notifications.
    */
    void SetErrorListener(CImageSourceErrorListener* listener);

};
```
