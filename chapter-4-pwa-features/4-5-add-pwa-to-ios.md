# Chapter 4 - Understanding PWA Features
## Lesson 5 - Add PWA to iOS

This lesson shows how to install your PWA to an iOS device.

For iOS we need to provide a new link to our icon image in the "index.html" file, which you can find in the "public" directory of your app.

In the &lt;head> section of "index.html" and a new &lt;link> tag following the existing favicon icon link.

[public/index.html]
<pre><code>
...
&lt;head>
...
&nbsp;&nbsp;&lt;link rel="apple-touch-icon" sizes="152x152" href="icon-152.png" />
...
</code></pre>

Next, run a new build of your app and serve it. But this time, instead of loading it in Chrome, you will use your iphone. When your ran "serve" it provided 2 addresses such as (http://localhost:5000 & http://192.168.0.2:5000). The second one is an IP address that you will enter into the Safari web browser on your iPhone. 

If all went well you should see your app in the Safari web browser.

Now at the bottom of the Safari browser window you should see the "share icon", which looks like a square box with an arrow pointing up. Click the share button, this brings up an iterface and you can scroll right until you see "Add to Home Screen". Click this and it will populate the title & show the icon we provided. There is also a button "add" to add this app to your device. As soon as you do that you should see an icon on your iPhone's home screen that you can click on to open your app.

If all went well the app icon is on your iPhone home screen and when you click it, Safari opens to display your React PWA app.

This is of course just for testing because as soon as we shut down our localhost server this will not work. For a production app you would need to deploy your app to a server to handle requests from you and others.
