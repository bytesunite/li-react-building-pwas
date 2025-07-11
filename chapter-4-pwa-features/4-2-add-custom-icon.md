# Chapter 4 - Understanding the PWA Manifest
## Lesson 2 - Add a Custom Icon

In the last lesson, when running a Lighthouse audit of the app, some warnings were displayed about not having a PNG icon. In this lesson we will try to clear some warnings by creating icons of different sizes for the application.

When you think about it, installing an app typically places an icon on your home screen that is used to launch the app. We need to create a couple different size icons for this purpose.

The instructor provides a moon image in the downloaded exercise files for the course. The original PNG size is 500 x 500. It is opened in the Preview app on the instructor's Mac computer. The image is resized and exported as a new image with new dimesions. Feel free to use your own image and image editing application for creating these icon images. Multiple sized images are created to match different device screen sizes. All files are saved to the "public" folder with files names that start with "icon-" and end with the dimension.<br>

The first file is saved as a PNG that is 120 x 120 and named "icon-120.png" so it is easily identified in our program files. This file is saved to the "public" folder of the the application.

This process is duplicated for creating mulitiple square images for sizes (120, 144, 152, 167, 180, 192, and 512) and they are all inside the "public" folder of the app.

With all these images ready to go, open the manifest file "public/manifest.json" and modify it as follows.

1. You can copy the first object for the "icons" property as we will paste it and modify it.<br><br>
    [public/manifest.json]
    <pre><code>...
    "icons": [
    &nbsp;&nbsp;{
    &nbsp;&nbsp;&nbsp;&nbsp;"src": "favicon.ico",
    &nbsp;&nbsp;&nbsp;&nbsp;"sizes": "64x64 32x32 24x24 16x16",
    &nbsp;&nbsp;&nbsp;&nbsp;"type": "image/x-icon"
    &nbsp;&nbsp;}
    ]</code></pre>

2. With the first one copied, pasted, and modified, we can copy this new object to create the others for the different sizes.<br><br>
    [public/manifest.json]
    <pre><code>...
    "icons": [
    &nbsp;&nbsp;{
    &nbsp;&nbsp;&nbsp;&nbsp;"src": "icon-120.png",
    &nbsp;&nbsp;&nbsp;&nbsp;"sizes": "120x120",
    &nbsp;&nbsp;&nbsp;&nbsp;"type": "image/png"
    &nbsp;&nbsp;},
    ...Other sizes go here...
    &nbsp;&nbsp;{
    &nbsp;&nbsp;&nbsp;&nbsp;"src": "favicon.ico",
    &nbsp;&nbsp;&nbsp;&nbsp;"sizes": "64x64 32x32 24x24 16x16",
    &nbsp;&nbsp;&nbsp;&nbsp;"type": "image/x-icon"
    &nbsp;&nbsp;}
    ]</code></pre>

With all the images added to the manifest file, create a new build and serve it. Then open it in a web browser and navigite to Chrome Dev Tools "Application" tab and click on "Manifest". If all went well, you should see all the images you just setup as part of the manifest information.

Run a LightHouse Audit and you should see the errors about PNG icons are gone.<br>
There are still errors that need to be addressed but the PNG icon errors should be resolved.
