# Chapter 3 - PWA Tools
## Lesson 4 - Going Offline

Go ahead a create a new build and start the server and open the web browser to the provided url. Then open Chrome Dev Tools and go to the Network tab. When you make a request you will see which resources are being requests. Anything that says "chunk" is a result of webpack that helped optimize our code into pieces. You will see a few files like the service-worker.js file, favicon.ico, etc. But the majority of what we see for this app is the individual requests for the videos.

So what happens if we take this app offline & how do we do that?<br>
In Chrome Dev Tools, under the Network tab, there is a checkbox "Offline" that we can check which will force a disconnect from the network.

If we force a refresh of our app the Network tab in Chrome Dev Tools will show a bunch of errors when attempting to go online and fetch the videos for our app. We also don't see any videos because we are disconnected from the network. The only thing we see is the page heading for our app, "Art Videos".

Go ahead an uncheck the "Offline" checkbox in the Network tab of Chrome Dev Tools. Hard refresh the page so it reloads the page with the videos.<br>

Next, we will download a video and save it to a location within our project. We will remove all code to fetch the videos and instead load that single video locally in our project.
1. In the browser click the icon (three vertical dots) on the first video displayed on the page and select "download". 
2. Go to your downloads folder on your computer and rename it "sculpture.mp4".
3. In your project directory create a new folder "src/videos" and move the video to this new folder.
4. Modify "src/App.js" to remove the Hooks and the code to fetch videos. Instead use a single tag.<br>
   WARNING: The instructor uses the wrong HTML syntax, not providing a nested source tag. The updated syntax is used below.<br>
   <div>
   [src/App.js]
   <pre><code>
   import './App.css';
   
   import video from './videos/sculpture.mp4';
   
   function App(){
   &nbsp;&nbsp;return (
   &nbsp;&nbsp;&nbsp;&nbsp;&lt;div className="App">
   &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;header>
   &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;h1>Art Videos&lt;/h1>
   &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/header>
   &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;video height={200} controls>
   &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;source src={video} type="video/mp4">
   &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Error! Your browser is unable to load the video
   &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/video>
   &nbsp;&nbsp;&nbsp;&nbsp;&lt;/div>
   &nbsp;&nbsp;)
   }
   
   export default App;</code></pre>
   </div>

5. Start your server with `npm start` and open a browser to make sure the video loads.<br>
   Then stop the server. 

   `my-application/$ npm start`
   
6. Now build your project and serve it to make sure it also works.
   <div><pre>
   my-application/$ npm run build
   my-application/$ serve -s build   (OR npm serve -s build)
   </pre>
   </div>


If all went well you should be able to see the video a play it.<br>
In the networking tab you can confirm by doing a hard reset that the service worker is running but we are not making http requests for the video resources.<br>

Go to the Chrome Dev Tools and in the Networking tag check the box "Offline". Perform a hard refresh the browser and the video should still be displayed and work.<br>
ATTENTION: take notice when you play the video, the "service worker" is involved in this request for media.

When your app MUST have resources available offline you are best to save them locally, like the video. Or you can cache items after the first load so that they are then made available offline and reduce the need to download them again when you are connected to the internet.
