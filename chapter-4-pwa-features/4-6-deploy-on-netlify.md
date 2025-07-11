# Chapter 4 - Understanding PWA Features
## Lesson 6 - Deploy on Netlify

[Netlify](https://www.netlify.com) is one option to deploy your web projects.

NOTE: The course shows this service is free but go to the website to confirm this and terms and service can change.

Netlify makes deploying React apps using a build folder fairly easy. First, if you have a GitHub account, you can log into Netlify without creating another account. It provides other login options such as BitBucket, GitLab, Google, etc. or an email address. 

Once you are logged in your are presented with an interface to create a new site. Netlify makes it possible to drag and drop your project's build folder from your computer to a target area on the website. And as simple as that it will create a new site for you. A url for your site is generated, such as "https://mygitusername.netlify.com", and you can open this in another web browser tab to try it out. You perform a Lighthouse audit by placing the url into an incognito or guest window. Notice that it creates an "https" address for us.

A Lighthouse Audit will show you meet all criteria (it is now https). However, the course video is outdated and Lighthouse no longer shows us the PWA interface that the instructor's video lessons are showing. Lighthouse has DEPRECATED the PWA interface since this course was released. Hopefully Lighthouse or another tool will bring back the PWA interface. As of July 2025 Lighthouse could use some work as it has been redesigned with less helpful messages than what the instructor is demonstrating in this course. 

If all went well you now have a PWA deployed online that others can use.
