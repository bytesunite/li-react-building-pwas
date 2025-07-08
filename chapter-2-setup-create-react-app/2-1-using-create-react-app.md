# Chapter 2 - Setup: Create React App
## Lesson 1 - Using create-react-app

The instructor mentions & uses one of the most popular React packages, called *create-react-app*. You can learn more about it at [create-react-app.dev](https://create-react-app.dev)

WARNING: create-react-app was DEPRECATED in Feb 2025. The course is outdated.<br>
You can still use it, but expect to see deprecation warnings.<br>

The Create React App is used to generate a React app. It provides all the scaffolding for creating a new React Project.<br>
The Create React App is also a PWA generator.

Lets setup a new React app using *create-react-app* that we will use for Chapter 2.

1. Create a new folder "ch2-cra-demo" in your local environment for your new react app.

2. Open this folder in your VSCode terminal and use npx to create a new React project.The name of your project "my-react-app", is specified after "create-react-app".<br>
Executing this command will require an internet connection and will take a minute or two to download the files for the new React app.<br>
    <div><pre>
    ch2-cra-demo/$ <code>npx create-react-app my-react-app</code></pre>
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
