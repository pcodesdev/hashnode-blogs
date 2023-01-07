# Create React App

*"Create React App"* is a command-line tool that creates a new React project for you. It sets up the development environment that you need to build a modern React app, including support for ES6 syntax, JSX, and a local development server. It's a quick and easy way to get started with a new React project, and it's the recommended way to create a new project if you're just starting with React.

To create a new React project using Create React App, you'll need to have Node.js and npm (the Node.js package manager) installed on your computer. Then, open a terminal and run the following command:

```javascript
 npx create-react-app my-app
```

Replace *"my-app"* with the name of your project. This will create a new directory with the same name as your project, and it will generate all the files you need to get started with your new React app.

Once the process is complete, you can navigate to the new project directory and start the development server by running the following commands:

```javascript
cd my-app
npm start
```

This will start the development server and open a new browser window with your React app. The new browser window opens at [http://localhost:3000/](http://localhost:3000/). You can start building your app right away!

when I start the development server and open a new browser window from the above local address I am presented with the following screen:

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1673077693883/de7bf006-cccd-4390-a964-10747b9fe793.png align="center")

The page will automatically reload if you make changes to the code. You will see the build errors and lint warnings in the console.

Three ways can be followed when creating a new react application:

### npx[​](https://create-react-app.dev/docs/getting-started#npx)

```javascript
npx create-react-app my-app
```

*(*[*npx*](https://medium.com/@maybekatz/introducing-npx-an-npm-package-runner-55f7d4bd282b) *comes with npm 5.2+ and higher, see* [*instructions for older npm versions)*](https://gist.github.com/gaearon/4064d3c23a77c74a3614c498a8bb1c5f)

### npm[​](https://create-react-app.dev/docs/getting-started#npm)

```javascript
npm init react-app my-app
```

`npm init <initializer>` is available in npm 6+

### Yarn[​](https://create-react-app.dev/docs/getting-started#yarn)

```javascript
yarn create react-app my-app
```

`yarn create` is available in Yarn 0.25+

## Selecting a package manager[​](https://create-react-app.dev/docs/getting-started#selecting-a-package-manager)

When you create a new app, the CLI will use [npm](https://docs.npmjs.com/) or [Yarn](https://yarnpkg.com/) to install dependencies, depending on which tool you use to run `create-react-app`. For example:

```javascript
# Run this to use npm
npx create-react-app my-app
# Or run this to use yarn
yarn create react-app my-app
```

## Output[​](https://create-react-app.dev/docs/getting-started#output)

Running any of these commands will create a directory called `my-app` inside the current folder. Inside that directory, it will generate the initial project structure and install the transitive dependencies:

```javascript
my-app
├── README.md
├── node_modules
├── package.json
├── .gitignore
├── public
│   ├── favicon.ico
│   ├── index.html
│   ├── logo192.png
│   ├── logo512.png
│   ├── manifest.json
│   └── robots.txt
└── src
    ├── App.css
    ├── App.js
    ├── App.test.js
    ├── index.css
    ├── index.js
    ├── logo.svg
    ├── serviceWorker.js
    └── setupTests.js
```

No configuration or complicated folder structures, only the files you need to build your app. Once the installation is done, you can open your project folder:

## npm test

`npm test` is a command that runs the test scripts defined in your package.json file. This command is typically used to run automated tests for your codebase.

For example, if you are using a testing library like Jest to test your React components, you can define a test script in your package.json file like this:

```javascript
{
  "scripts": {
    "test": "jest"
  }
}
```

Then you can run your tests by entering the following command in your terminal:

```javascript
npm test
```

This will run all the tests in your codebase and display the results in the terminal. If you want to run a specific test or a group of tests, you can pass the name of the test or the test pattern as an argument to the `npm test` command. For example:

```javascript
npm test -- testName
```

```javascript
npm test -- testName.test.js
```

```javascript
npm test -- "pattern*"
```

You can also use the `--watch` flag to run your tests in watch mode, which means that the tests will be re-run every time you make a change to your code. This is useful during development as it allows you to quickly see the impact of your changes on the tests.

```javascript
npm test -- --watch
```

## npm run build

`npm run build` is a command that creates a production-ready version of your app. It optimizes your code for deployment and reduces the size of your JavaScript and CSS files.

The `build` script is typically defined in the `scripts` section of your package.json file. For example:

```javascript
{
  "scripts": {
    "build": "react-scripts build"
  }
}
```

The `react-scripts` package is a set of scripts provided by the Create React App tool that is used to build and run your React app.

To create a production build of your app, navigate to the root directory of your project and run the following command:

```javascript
npm run build
```

This will create a `build` directory in your project with an optimized version of your app. You can then deploy this build to a web server or host it on a platform like GitHub Pages.

The build process includes the following optimizations:

* Code minification: reduces the size of your JavaScript and CSS files by removing unnecessary whitespace and comments.
    
* Source mapping: enables you to debug your production code as if it were the unminified version.
    
* File hashing: adds a unique hash to the names of your files to prevent browser caching issues.
    

You can also pass additional options to the build script to customize the build process. For example, you can use the `--report` flag to generate a report on the size and performance of your app.

```javascript
npm run build -- --report
```

## Conclusion

In conclusion, Create React App is a great tool for getting started with React quickly and easily. It allows you to create a new React app with zero configuration, and it provides a development server and a set of scripts for building and testing your app.

To create a new React app using Create React App, you'll need to have Node.js and npm (the Node.js package manager) installed on your computer. Then, open a terminal window and enter the following command:

```javascript
npx create-react-app my-app
```

Replace "my-app" with the name you want to give to your app. This will create a new directory with the same name as your app, and it will generate all the files you need to get started with a new React app.

Once the command finishes running, navigate to the app directory by running the following command:

```javascript
cd my-app
```

Then start the development server by running:

```javascript
npm start
```

This will open a new browser window with your React app running on it.

You can then start building your app by modifying the files in the `src` directory. When you're ready to deploy your app, you can use the `npm run build` command to create a production-ready version of your app in the `build` directory.