# React.js

## React的特点

1. 声明式的视图层
2. 简单的更新流程
3. 灵活的渲染实现
4. 高效的DOM操作

## Development Environment for React

Basic Environment: 

- Node.js: https://nodejs.org
- NPM, also Yarn (https://yarnpkg.com)

Supplement Environment:

- Webpack: JavaScript module packaging tool
- Babel: a JavaScript intepretor
- ESLine: JavaScript code checking tool
- Code Editor

## [Create a new React App](https://reactjs.org/docs/create-a-new-react-app.html)

```bash
npx create-react-app my-app
cd my-app
npm start
```

Create React App doesn't handle backend logic or databases; it just creates a frontend build pipeline, so you can use it with any backend your want.

Learning repo is [here](https://github.com/yasenstar/learn_webdev/tree/main/react)

After creating, below are the key files contents --

File: /src/index.js

```javascript
import React from 'react';
import ReactDOM from 'react-dom/client';
import './index.css';
import App from './App';
import reportWebVitals from './reportWebVitals';

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(
  <React.StrictMode>
    <App />
  </React.StrictMode>
);

// If you want to start measuring performance in your app, pass a function
// to log results (for example: reportWebVitals(console.log))
// or send to an analytics endpoint. Learn more: https://bit.ly/CRA-vitals
reportWebVitals();
```

File: App.js

```js
import logo from './logo.svg';
import './App.css';

function App() {
  return (
    <div className="App">
      <header className="App-header">
        <img src={logo} className="App-logo" alt="logo" />
        <p>
          Edit <code>src/App.js</code> and save to reload.
        </p>
        <a
          className="App-link"
          href="https://reactjs.org"
          target="_blank"
          rel="noopener noreferrer"
        >
          Learn React
        </a>
      </header>
    </div>
  );
}

export default App;
```

File: /public/index.html

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8" />
    <link rel="icon" href="%PUBLIC_URL%/favicon.ico" />
    <meta name="viewport" content="width=device-width, initial-scale=1" />
    <meta name="theme-color" content="#000000" />
    <meta
      name="description"
      content="Web site created using create-react-app"
    />
    <link rel="apple-touch-icon" href="%PUBLIC_URL%/logo192.png" />
    <!--
      manifest.json provides metadata used when your web app is installed on a
      user's mobile device or desktop. See https://developers.google.com/web/fundamentals/web-app-manifest/
    -->
    <link rel="manifest" href="%PUBLIC_URL%/manifest.json" />
    <!--
      Notice the use of %PUBLIC_URL% in the tags above.
      It will be replaced with the URL of the `public` folder during the build.
      Only files inside the `public` folder can be referenced from the HTML.

      Unlike "/favicon.ico" or "favicon.ico", "%PUBLIC_URL%/favicon.ico" will
      work correctly both with client-side routing and a non-root public URL.
      Learn how to configure a non-root public URL by running `npm run build`.
    -->
    <title>React App</title>
  </head>
  <body>
    <noscript>You need to enable JavaScript to run this app.</noscript>
    <div id="root"></div>
    <!--
      This HTML file is a template.
      If you open it directly in the browser, you will see an empty page.

      You can add webfonts, meta tags, or analytics to this file.
      The build step will place the bundled scripts into the <body> tag.

      To begin the development, run `npm start` or `yarn start`.
      To create a production bundle, use `npm run build` or `yarn build`.
    -->
  </body>
</html>
```

## Deploy React to Azure Web App

1. Open your Project in VS code
2. Go to Extensions. Search for Azure App Service and click installed
3. Go to Azure App Service. Sign in to your Azure Account
4. Create one App Service in Azure portal beforehand
5. Click on Deploy to Web App
6. Select your Subscription, select App Service
7. Select local folder to Deploy
8. Now you should be able to deploy your React app to Azure App Service

Thanks [Harshitha Veeramalla](https://stackoverflow.com/questions/69892360/how-to-deploy-react-to-azure-web-app-using-the-azure-app-service-plugin-in-visua#:~:text=Steps%20to%20deploy%20React%20to%20Azure%20Web%20App,deploy%20your%20react%20app%20to%20Azure%20App%20Service)

