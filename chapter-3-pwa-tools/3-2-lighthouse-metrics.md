# Chapter 3 - PWA Tools
## Lesson 2 - Lighthouse Metrics

The last lesson showed how to run an audit of a website with Google's Lighthouse. Let's start up our app and run Lighthouse and see what we get.

NOTE: The following instructions have replaced the courses DEPRECATED Chrome Dev Tools instructions with the current syntax.<br>
Always check the documentation for the latest syntax for Lighthouse at [Lighthouse Documentation](https://developer.chrome.com/docs/lighthouse/)

NOTE: To open an *incognito* window in Chrome you can go to `File/New Incognito Window` from the main menu. If you do not see the main menu you can look for the icon (three vertical dots) that is in the upper right of Chrome, and select "New Incognito Window".

NOTE: To open guest mode in Chrome, click on the profile icon (looks like a person with head/shoulders) then navigate to "Open Guest Profile". 

It is suggested to run Google's Lighthouse tool in either incognito or guest mode. This is to prevent any browser extensions or settings interfering with the Lighthouse audit.

1. Start up your server on localhost using:<br>
   `my-application/$ npm run start`
2. Open the Chrome web browser & open a new incognito window/tab (or guest mode window). Navigate to the url provided by the last command
4. Open Chrome Dev Tools, navigate to the "Lighthouse" tab
5. Click on "Analyze page load"

The results are not that great, but that gives us room for improvement.

One suggestion provided by the audit is to "minify JavaScript". When you build a project for production, this is one step that is performed for you. It will refactor your JavaScript to remove all whitespace and optimize the code for performance rather than readability.

Another suggestion for the audit is that a PWA should be using "https". The current running server is using the "http" protocol.

Make a note of the Audit results so we can compare it with our build folder. For example:
- Performance: 86
- Accessibility: 100
- Best Practices: 86
- SEO: 80

So what happens when we run this on the "build" folder, when we build this project for production?

Remember, we will building our PWA project for production, so in this case the steps are slightly different. Create a new build & start the server again.

First, stop your running server (CTRL + C) in the terminal. Then create a new build, start the server and re-run the audit in a Chrome incognito window.<br>
ATTENTION: If you did NOT install server globally use `npx serve -s build`
1. my-application/$ `npm run build`
2. my-application/$ `serve -s build`
3. Open the Chrome web browser & open a new incognito window/tab (or guest mode window). Navigate to the url provided by the last command
4. Open Chrome Dev Tools, navigate to the "Lighthouse" tab
5. Click on "Analyze page load"

You should see performance jump, but everything else looks about the same. This is because the build process performed "minification" of our JavaScript code.

For example:
- Performance: 100
- Accessibility: 100
- Best Practices: 86
- SEO: 80

In upcoming lessons we will explore how we can take additional steps to make our PWA app conform to things such as "https", worke offline, etc.
