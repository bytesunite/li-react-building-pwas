# Chapter 4 - Understanding PWA Features
## Lesson 3 - Change the Name of the App

In your manifest file you will see both a "short_name" and "name" for your application. The short name is meant to be about 12 characters and the name is about 45 characters. When creating a new React PWA app the name is provided for you but you can change this by modifying the manifest file.

[public/manifest.js]
<pre><code>
...
"short_name": "ArtVideos",
"name": "Art Videos for Fun and Learning",
...
</code></pre>

If you build and run this you can got into Chrome Dev Tools, go to the "Application" tab and click on "Manifest" to see the updated app name.

The name is what will be displayed when you install it on devices.
