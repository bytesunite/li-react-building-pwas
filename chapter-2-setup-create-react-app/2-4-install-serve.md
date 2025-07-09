# Chapter 2 - Create React App
## Lesson 4 - Install Serve

Create React App creates a scaffold for new apps. One of those files is called "package.json", which includes information about dependencies used by the application. If you open this file, you will find a "Scripts" property with (start, build, test, eject). We have already used "start" to run our app. But the "build" process is used when preparing your app for production.<br>

When creating a PWA you will need to run `npm build` to run the app through a production process. The we will need to serve that build folder to run our app on a specific localhost port. A npm package called "serve" can be used to do just that, serve results of the build folder to run the app.<br>

The Npm package [serve](https://www.npmjs.com/package/serve) in the npm registry is described as follows:<br>
"serve helps you serve a static site, single page application, or just a static file (no matter if on your device or on the local network). It also provides a neat interface for listing the directory's contents".

If your server is currently running, stop in by going to the terminal where you started in and press `Ctrl + C`.

The instructor shows how to install the *serve* package globally, but you can also choose to install it locally for a project.

Locally (project): To prevent polluting the global environment I will run the serve package locally. When you install packages locally you can install different versions for each project. When you install globally you are limited to a single version.<br>
NOTE: "npx" (not "npm") is used to run a command from a local or remote npm package. It will execute node.js packages directly from the npm registry (or a local package) without needing to install them globally on your system. This is useful for running one-time commands or trying out packages without cluttering your environment. First is <br>
`my-application/$ npx serve`

Globally (environment): The instructor installed it this way:<br>
`my-application/$ sudo npm install -g serve`


In the next lesson you will learn how to run `serve <build folder name>` to start the server for your project using the folder created by the build process.
