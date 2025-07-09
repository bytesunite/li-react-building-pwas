# Chapter 2 - Setup: Create React App
## Lesson 5 - Run a Build

In the last lesson the *serve* package was installed. Now we will build our app and serve it on a localhost port to execute the app.

The first step is to build our app using the build script that was made available when we created a new project with Create React App.

`my-application/$ npm run build`

You will see the build process start and a message letting you know the "build" folder is ready to be deployed. It says you may serve it with a static server using the syntax:

    serve -s build

Next, run this command in the terminal to start serving your build. Then open a web browser and use the url provided by the running the command. It will provide a url such as "http://localhost:5000/" or "http://localhost:3000/".

`my-application/$ serve -s build`

NOTE: If you did not install the *serve* package globally you can use the following:<br>

`my-application/$ npx serve -s build`

If all went well you should see your app running in the browser. Also, if you are using the browser extension for React it should let you know you are running a "production" React page.

If you go back to your file explorer you should see a "build" folder with files that were created as part of the build process.
