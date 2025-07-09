# Chapter 3 - PWA Tools
## Lesson 1 - Using Lighthouse

*Lighthouse* is a tool created by Google to help improve the quality of web pages. <br>
[Lighthouse](https://developer.chrome.com/docs/lighthouse)


(Google: Not part of the course)<br>
Google's Lighthouse Description:<br> 
Lighthouse is an open-source, automated tool to help you improve the quality of web pages. You can run it on any web page, public or requiring authentication. It has audits for performance, accessibility, SEO, and more.

To run Lighthouse in Chrome DevTools, Google provides the following:<br>
(Lighthouse has its own panel in Chrome Dev Tools)<br>
1. Download Google Chrome for Desktop
2. Open Chrome, and go to the URL you want to audit. You can audit any URL on the web.
3. Open Chrome Dev Tools
4. Click on the **Lighthouse** tab
5. Click on **Analyze page load**. DevTools shows you a list of audit categories. Leave them all enabled.
6. Click **Run audit**. After 30 to 60 seconds, Lighthouse gives you a report on the page.

NOTE: Google suggests you open a new Chrome Incognito Window to prevent stored data that may impact loading performance.<br>
(end Google Description)

ATTENTION: The instructor shows an "Audits" tab, which Google has DEPRECATED since this course was released. It now uses a "Lighthouse" tab & may change in the future. Google is already warning that audits will soon be replaced with *Insights*.
The point is things are always changing so always check the documentation for whatever tool you are using. It's likely the course instruction/videos are outdated.

The instructor runs the Lighthouse audit as follows:
1. Opens up a Chrome browser and navigates to "https://www.airbnb.com"
2. Opens Chrome Dev Tools and navigates to the "Audits" tab (Currently the "Lighthouse" tab. The "Audits" tab is DEPRECATED) 
3. Click on "Run Audits" (Currently called "Analyze page load")

After a minute or two a report is generated for the page, providing a score and details on topics such as:
- Performance
- Accessibility
- SEO

The report shows that airbnb.com has poor performance scores but has excellent scores for accessibility, best practices, and SEO. This score is similar in the current version of Lighthouse as the version the instructor is using some metric names are different or missing.<br>
Even though the results are different than the instructors, you can still interpret the results of the audit and gain insights via Lighhouse's suggestions for improvement.

The instructor points out if you run this tool a few times that the results can be mixed so you always want to perform addition tests and test and different devices.
