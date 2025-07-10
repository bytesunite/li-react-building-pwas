# Chapter 2 - Setup: Create React App
## Lesson 1 - Using create-react-app

The instructor mentions & uses one of the most popular React packages, called *create-react-app*. You can learn more about it at [create-react-app.dev](https://create-react-app.dev)

WARNING: create-react-app was DEPRECATED in Feb 2025. The course is outdated.<br>
You can still use it, but expect to see deprecation warnings.<br>

The Create React App is used to generate a React app. It provides all the scaffolding for creating a new React Project.<br>
The Create React App is also a PWA generator.

Lets setup a new React app using *create-react-app* that we will use for Chapter 2 (and Chapter 3).

<span style="color:red;">WARNING</span>: The instructor fails to explain templates, which are used to automatically generate a serviceWorker.js file needed later in Chapter 3.<br>
REFERENCE: https://create-react-app.dev/docs/making-a-progressive-web-app/<br>
<span style="color:green;">Correction</span>:<br> 
`npm create-react-app my-application --template cra-template-pwa`<br>


1. Create a new folder "ch2-cra-demo" in your local environment for your new react app.

2. Open this folder in your VSCode terminal and use npx to create a new React project.<br>
CORRECTION: When creating a React PWA, use "--template cra-template-pwa".<br>

Executing this command will require an internet connection and will take a minute or two to download the files for the new React app.<br>
    <div><pre>
    ch2-cra-demo/$ <code>npx create-react-app my-react-app --template cra-template-pwa</code></pre>
    </div>

3. Navigate to your new React project's directory "my-react-app".
    <div><pre>
    ch2-cra-demo/$ <code>cd my-react-app</code>
    ch2-cra-demo/my-react-app/$</pre>
    </div>

4. List the folder contents to show the files that were created<br>
    <div><pre>
    ch2-cra-demo/my-react-app/$ <code>ls</code>
    <samp>package.json
    node_modules
    src
    ...</samp></pre>
    </div>
       

In the next lesson we will start using this scaffold.
