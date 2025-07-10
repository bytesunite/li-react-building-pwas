# Chapter 4 - Understanding PWA Features
## Lesson 1 - Understanding the PWA Manifest

Your project directory has a folder named "public" with a file named "manifest.json". This file is a very important part of creating a PWA. This file contains a bunch of meta-data about the application.

To explore your application manifest we can use Chrome Dev Tools. Clicking the "Application" tab will give you access to "Manifest". Clicking this will display details about your application manifest.<br>
At the top you will find a url to your manifest file, which will open a new window to display its content. Below this link you can see details about your application such as the name, theme color, etc.

The instructor builds the app again then runs Lighthouse. A few things are pointed out:
- Manifest does not have a PNG icon of at least 192px
- Does not use https

In the upcoming lessons these errors/warnings will be addressed by exploring the manifest file.
