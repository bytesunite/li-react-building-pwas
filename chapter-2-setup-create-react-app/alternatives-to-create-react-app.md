# My Notes (NOT PART OF THE COURSE)
## Alternatives to the DEPRECATED create-react-app

WARNING:<br>
Unfortunately *create-react-app* was DEPRECATED in February of 2025. You can read more about this at [deprecating create-react-app](https://react.dev/blog/2025/02/14/sunsetting-create-react-app)

This course has yet to be updated.<br>
To continue with this course, you can still use *create-react-app* but you will see deprecation warnings.

Modern solutions include:
- The next.js framework [nextjs pwa](https://nextjs.org/docs/app/guides/progressive-web-apps)
- The Remix framework [remix pwa](https://remix.run/resources/remix-pwa)
- Vite build tool using the pwa plugin [vite-plugin-pwa](https://www.npmjs.com/package/vite-plugin-pwa)


To create a new React app with Vite and the PWA plugin, follow the steps below:
1. create a new Vite project
    <div>
    <pre>/$ <code>npm create vite@latest my-react-app -- --template react</code></pre>
    </div>


2. change to the project directory & install dependencies<br>
    <div>
    <pre>/$ <code>cd my-react-app</code>
   my-react-app/$ <code>npm install</code></pre>
    </div>

3. install vite-plugin-pwa<br>
    <div>
    <pre>my-react-app/$ <code>npm install vite-plugin-pwa --save-dev</code></pre>
    </div>

4. configure Vite, add plugin to vite.config.js<br>
    <div>
    <pre><code>import { VitePWA } from 'vite-plugin-pwa'

    export default {
    &nbsp;&nbsp;plugins: [
    &nbsp;&nbsp;&nbsp;&nbsp;VitePWA()
    &nbsp;&nbsp;]
    }</code></pre>
    </div>

5. Customize options. Modify the plugin options to fit your app's requirements, such as defining the web app manifest. Documentation can be found here [vite-plugin-pwa](https://www.npmjs.com/package/vite-plugin-pwa)
