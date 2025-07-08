# Chapter 2 - Setup: Create React App
## Lesson 2 - Create an App Component

NOTE:<br>
This course provides exercise files that you can download from the LinkedIn Learning course. Every chapter has folder for each lesson * contains two nested folders (start, finished). None of them include a "node_modules" folder to reduce the file size for the course examples zip file. This also means once you load the folder into VSCode you will navigate to the "my-application" directory and run `npm install` before working with the project.

At this point I am not going to download the course exercises zip file, but simply follow along creating my own app and update it lesson by lesson.

With this said, the next step is to start the server and view the React app that was created in the previous lesson.

Run the "start" script from your project folder "my-react-app" to start the server. It also opens your default web browser or a new tab in the open web browser to the address: "http://localhost:3000".<br>
<div><pre>
ch2-cra-demo/my-react-app/$ npm start
Starting the Development Server...
</pre></div>

If all went well, you will see a spinning React logo with a message below it saying "Edit src/App.js and save to reload". There is also a link that says "Learn React" that points to "reactjs.org".

NOTE: If you need to to stop the server you can press Ctrl+C in the terminal.

Lets explore the scaffolding. Go to your file explorer and open the "index.js" file inside the "src" folder. This JavaScript file is responsible for grabbing a div tag with the id of "root" from "index.html" and inserting what is known as a *React Component* into the DOM.

Next, you can look in the "index.html" file and see it has a div tag with the id of "root", which aligns with the "index.js" file's getElementById value.

The root component is "App.js", inside the "src" folder. If you look at this file you will see the content that was displayed in the browser.

So let's modify the App component to display a h1 tag with the text "Videos". When you save these changes, you should see the web browser has automatically updated your app with these new changes. This feature is automatically reloading the page after saving changes is known as "Hot Module Reloading(HMR)".<br>

[src/App.js]
<pre><code>
import React from 'react';
import './App.css';

function App(){
  return (
    &lt;div className="App">
      &lt;header>
        &lt;h1>Videos&lt;/h1>
      &lt;/header>
    &lt;/div>
  );
}

export default App;
</code>
</pre>


If all went well, you should see the React app now displays a single heading of "Videos".

Next we can modify the "App.css" file to update the styling of the heading. To speed things along we will not change much except to replace ".App-header" to simply "header" to apply styles to the header tag. We can also change the "min-height" of the header to "20vh". After making these changes you should see the styles applied to the heading.<br>

[App.css]
<pre>
...
header {
  ...
  min-height: 20vh;
}
</pre>

If all went well you should see the CSS styles applied to the heading in the browser after you save the file.

