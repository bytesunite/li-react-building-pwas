# Chapter 3 - PWA Tools
## Lesson 3 - Register The Service Worker

When learning about what PWAs are you here about "Service Workers". A *Service Worker* is a script that your browser runs in the background to perform various tasks. Essentially it is a JavaScript file that does things like caching resources, handling network requests, & storing content for offline use.

1. Start up your server on your build folder<br>
   my-application/$ `serve -s build`

2. Open up a web browser to the URL returned by the previous command.

3. Open Chrome Dev Tools and navigate to the "Application" tab. Here you will find "Service Workers". This is where you can see a list of service workers. You are also provided a way to "unregister" a specific service work if you choose to.

Create React App will provide a service worker file "src/serviceWorker.js" by default (when you supply a file or you use a template).<br>

ATTENTION: Chapter 2 failed to show how to use a template to create the React PWA project. Make sure you created your app with the "--template cra-template-pwa" template or you will NOT see a serverWorker.js file. You also want to modify "index.js" to comment out the import and execution to "reportWebVitals" to prevent errors. (see my alternatives-to-create-react-app.md file for replacing CRA with Vite or NextJS)

After correcting your React app by using a PWA template, we can continue... (hopefully you saw my correction to the instructor's failure to mention the PWA template back in Ch2) 

Look inside the "src/index.js" file you will see it imports content from the "serviceWorker.js" file.<br>
This Service Worker is known as "opt-in", meaning you have to register the Service Worker to use it.

To register a Service Worker in Create React App, navigate to the "index.js" file and change the last line to use "register()". Then save the file.<br>
BEFORE: `serviceWorker.unregister();`<br>
AFTER: `serviceWorker.register();`

After registering the Service Worker, create a new build of your project & start up the server to view the Service Workers in Chrome Dev Tools.
1. my-application/$ `npm run build`
2. my-application/# `serve -s build` (OR: `npx serve -s build`)
3. Open a new browser to the URL provided
4. Navigate to the "Application" tab, then to "Services Workers". You should see a new service worker "service-worker.js", that was not there before.

If you were able to enable the service worker and see in in Chrome Dev Tools under Application/Service Workers, let's continue...

Next, lets update "App.js" with a simple change such as updating the heading text to "Art Videos", then save the file.

[src/App.js]<br>
...<br>
&lt;h1>Art Videos&lt;/h1><br>
...

After making this change, rebuild the app and serve it again. Then refresh the page. What you should see is that the title is the same it was before (Videos) instead of the updated "Art Videos". This is what is known as *caching*.<br>
So what is going on? Previously, before we were running a build process, updates were immediately rendered with help of Hot Module Reloading. So how do we get around this?<br>
1. You can close the browser window, open a new browser window, then make a new request.
2. You can do a hard refresh
   - Win: Ctrl + Shift + R
   - Mac: Cmd + Shift + R
   - You can also hold down Shift and click on the refresh icon (a circular arrow) next to the URL in the address bar

