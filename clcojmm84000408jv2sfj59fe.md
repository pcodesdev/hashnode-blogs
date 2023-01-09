# Reactjs Editor Setup and Developer Tools

A properly configured editor can make code clearer to read and faster to write. It can even help you catch bugs as you write them! If this is your first time setting up an editor or you’re looking to tune up your current editor, I have a few recommendations.

## Your Editor

VS Code is a free, open-source source code editor developed by Microsoft for Windows, Linux, and macOS. It includes support for debugging, version control, and an integrated terminal. VS Code also has a large library of extensions that provide additional functionality, such as support for additional programming languages and tools. Some of the features of VS Code include:

* IntelliSense: provides smart completions based on variable types, function definitions, and imported modules.
    
* Debugging: this allows you to set breakpoints, step through code, and see the value of variables as you debug.
    
* Refactoring provides tools for restructuring and optimizing your code.
    
* Integrated terminal: allows you to open a terminal window directly within VS Code.
    
* Git integration: provides tools for working with Git repositories, including the ability to stage, commit, and push changes.
    

%[https://code.visualstudio.com/] 

You can download the visual studio code from the link above.

Other popular text editors used in the React community include:

* [WebStorm](https://www.jetbrains.com/webstorm/) is an integrated development environment designed specifically for JavaScript.
    
    %[https://www.jetbrains.com/webstorm/] 
    
* [Sublime Text](https://www.sublimetext.com/) has support for JSX and TypeScript, [syntax](https://stackoverflow.com/a/70960574/458193) highlighting and autocompletes built in.
    

%[https://www.sublimetext.com/] 

* [Vim](https://www.vim.org/) is a highly configurable text editor built to make creating and changing any kind of text very efficient. It is included as “vi” with most UNIX systems and with Apple OS X. [https://www.vim.org/](https://www.vim.org/)
    

## **Recommended text editor features**

### **Linting**

Linting is the process of running a program that analyzes your source code for potential issues, such as syntax errors, style violations, and logical errors. Linting can help identify problems with your code that may not be immediately apparent and can help you write more consistent reliable code.

In VS Code, linting is provided by extensions that use static analysis to check your code. There are many different linting extensions available for VS Code, each with its own set of rules and configurations. To enable linting in VS Code, you will need to install a linting extension and configure it to run on your code.

To install a linting extension in VS Code, open the Extensions tab <mark>(Ctrl+Shift+X)</mark> and search for "linting" in the marketplace. Once you have found an extension you would like to use, you can install it by clicking the "Install" button. After installing the extension, you will need to configure it to run on your code. This typically involves setting the appropriate file patterns and rules in the extension's configuration settings.

Once you have configured a linting extension, it will automatically run on your code as you edit it, highlighting any issues it finds. You can also manually run the linter by using the appropriate command from the Command Palette <mark>(Ctrl+Shift+P</mark>).

[ESLint](https://eslint.org/) is a popular, open-source linter for JavaScript.

* [Install ESLint with the recommended configuration for React](https://www.npmjs.com/package/eslint-config-react-app) (be sure you have [Node installed!](https://nodejs.org/en/download/current/))
    
* [Integrate ESLint in VSCode with the official extension](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)
    

**Make sure that you’ve enabled all the** [`eslint-plugin-react-hooks`](https://www.npmjs.com/package/eslint-plugin-react-hooks) rules for your project. They are essential and catch the most severe bugs early. The recommended [`eslint-config-react-app`](https://www.npmjs.com/package/eslint-config-react-app) preset already includes them.

### **Formatting**

Formatting refers to the process of arranging your code in a specific, consistent style. This can include things like indentation, whitespace, and line breaks. Proper formatting can help make your code more readable and easier to understand for yourself and others who may be working on the same codebase.

VS Code includes several formatting options that you can use to automatically reformat your code. To format your code, you can use the "Format Document" command from the Command Palette (Ctrl+Shift+P) or by right-clicking the text editor and selecting "Format Document" from the context menu.

VS Code also includes several formatting extensions that you can use to customize the formatting of your code. These extensions allow you to set specific formatting rules and options, such as indentation style and line wrapping. To install a formatting extension, you can search for "formatting" in the Extensions tab (Ctrl+Shift+X) and install the extension you would like to use. Once you have installed a formatting extension, you can configure it by setting the appropriate options in the extension's configuration settings.

Formatting can also be controlled by your code's linting rules. Some linting extensions include rules for formatting and will highlight any formatting issues they find as you edit your code.

Nowadays visual studio code comes preconfigured with **prettier** which is the official code formater for visual studio code.

#### **Formatting on save**

Ideally, you should format your code on every save. VS Code has settings for this!

1. In VS Code, press `CTRL/CMD + SHIFT + P`.
    
2. Type “settings”
    
3. Hit Enter
    
4. In the search bar, type “format on save”
    
5. Be sure the “format on save” option is ticked!
    

> If your ESLint preset has formatting rules, they may conflict with Prettier. We recommend to disable all formatting rules in your ESLint preset using [`eslint-config-prettier`](https://github.com/prettier/eslint-config-prettier) so that ESLint is *only* used for catching logical mistakes. If you want to enforce that files are formatted before a pull request is merged, use [`prettier --check`](https://prettier.io/docs/en/cli.html#--check) for your continuous integration.

# **React Developer Tools**

React Developer Tools is a browser extension for Chrome and Firefox that allows you to inspect the React component tree of your application in the browser's developer console. With React Developer Tools, you can view the props and state of individual components, trace the component hierarchy, and see the component's source code. This can be helpful when debugging your React application or understanding how it is structured.

To install React Developer Tools in Chrome, you can go to the Chrome Web Store and search for "React Developer Tools". Once you have found the extension, click the "Add to Chrome" button to install it. After installing the extension, you will need to refresh any open tabs for the extension to take effect.

To install React Developer Tools in Firefox, you can go to the Firefox Add-ons website and search for "React Developer Tools". Once you have found the extension, click the "Add to Firefox" button to install it. After installing the extension, you will need to restart Firefox for the extension to take effect.

Once you have installed React Developer Tools, you can access it by opening the developer console in your browser and selecting the "React" tab. This will open the React Developer Tools panel, which you can use to inspect the React components of your application.

If you visit a website **built with React,** you will see the *Components* and *Profiler* panels.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1673251167072/e6f4d5eb-0936-4164-9478-73eee8e63612.png align="center")

### **Safari and other browsers**

For other browsers (for example, Safari), install the [`react-devtools`](https://www.npmjs.com/package/react-devtools) npm package:

```javascript
#Yarn yarn global add react-devtools 
#Npm npm install -g react-devtools
```

Next, open the developer tools from the terminal:

```javascript
react-devtools
```

Then connect your website by adding the following `<script>` tag to the beginning of your website’s `<head>`:

```javascript
<html>
  <head>    
      <script src="http://localhost:8097"></script>
```

Reload your website in the browser now to view it in developer tools.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1673251397229/b8e73462-ca28-4154-8bfb-ac986750b372.png align="center")

## Conclusion

To set up a React development environment, you will need to have a code editor and some developer tools installed on your computer. VS Code is a popular choice for a code editor for React development, as it includes support for debugging, version control, and an integrated terminal. You can also enhance VS Code with extensions that provide additional functionality, such as support for additional programming languages and tools.

React Developer Tools is a browser extension that you can use to inspect the React components of your application in the browser's developer console. It allows you to view the props and state of individual components, traces the component hierarchy, and see the component's source code. This can be helpful when debugging your React application or understanding how it is structured.

Overall, setting up a React development environment involves installing and configuring a code editor and developer tools to meet your specific needs. With the right tools in place, you will have everything you need to start building and debugging your React applications.