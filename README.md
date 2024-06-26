# Swift Metal Camera / iOS Metal Video Generator / Metal Image Generation

You are here because you want to...

1. How to upload camera feed direct to metal kernel/fragment functions.
2. Give a start with basic Still Image Texture / Camera Metal Texture loading/processing in iOS graphics using metal API(s).
3. Read a `MTLTexture` buffer, Then use the buffer to create a `CVPixelBuffer`/`UIImage` and whatever you like.
4. If you are frustrated to understand the metal kernel functionalities and how it should be calculated; then please give a look to this official document from Apple: https://developer.apple.com/documentation/metal/setting_up_a_command_structure
5. If you would like to read more from the following link then it will be easier to understand the basic of Metal GPU pipeline: https://developer.apple.com/documentation/metal/setting_up_a_command_structure
6. Metal shaders for blending and applying effects

![Meta Video](https://github.com/mostafizurrahman/metal-camera-metal-video-metal-image/blob/master/IMG_40DE310CE676-1.jpeg)

## Basic is grabbed from here :: https://github.com/navoshta/MetalRenderCamera

I grabbed camera session, metal texture cache creation and other setup related code from here. I perform subclassing for `MTLCommandEncoder` class. I subclassed `AVAssetWriter` to generate video from `MTLTexture`. 
Here are some important notes about the metal rendering process

1. Metal Texture used for rendering in `MTLView` is not suitable for generating video/still image.
2. `MTLComputeCommandEncoder` is used to process camera feed in metal kernel function. 
3. The output is written to an internal texture for rendering and later video/image generation.
4. Kernel function subclassing for applying the different effect in live iOS camera stream.
5. If you would like to add some custom metal effects you my subclass `BaseKernelPipelineState` and override `processArguments(computeEncode:)` method. 

* Any Contribution and Suggestion about metal will be highly appreciated.

#### contact @ mostafizur.cse@gmail.com // +8801675876752
# Camera_Metal_Pro
