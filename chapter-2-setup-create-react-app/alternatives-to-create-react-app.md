# My Notes (NOT PART OF THE COURSE)
## Alternatives to the DEPRECATED create-react-app

WARNING:<br>
Unfortunately *create-react-app* was DEPRECATED in February of 2025. You can read more about this at [deprecating create-react-app](https://react.dev/blog/2025/02/14/sunsetting-create-react-app)

This course has yet to be updated.<br>
To continue with this course, you can still use *create-react-app* but you will see deprecation warnings.

Modern solutions include:
- The next.js framework [nextjs pwa](https://nextjs.org/docs/app/guides/progressive-web-apps)
- The Remix framework [remix pwa](https://remix.run/resources/remix-pwa)
- Vite framework using the pwa plugin [vite-plugin-pwa](https://www.npmjs.com/package/vite-plugin-pwa)


To create a new React app with Vite and the PWA plugin, follow the steps below:
1. create a new Vite project
  
    /$ npm create vite@latest my-react-app -- --template react

2. install dependencies

    /$ cd my-react-app
    my-react-app/$ npm install

3. install vite-plugin-pwa

    my-react-app/$ npm install vite-plugin-pwa --save-dev

4. configure Vite, add plugin to vite.config.js

    import { VitePWA } from 'vite-plugin-pwa'

    export default {
      plugins: [
        VitePWA()
      ]
    }

5. Customize options. Modify the plugin options to fit your app's requirements, such as defining the web app manifest.<br>
Documentation can be found here [vite-plugin-pwa](https://www.npmjs.com/package/vite-plugin-pwa)

