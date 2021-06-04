# Install Chrome, Node, IDE
For participation you need a notebook with MacOS, Windows or Linux.

Please install the following tools:

1. Install current version of Chrome (used for Angular developer tools)

    Download the installer here: https://www.google.com/intl/en/chrome/browser/

    Install Augury as a Chrome Extention

2. Install current version of Node.js and NPM (version >= 8)

    Download the installer here: http://nodejs.org/download/

    If you have to configure a proxy: https://docs.npmjs.com/misc/config#https-proxy

3. Install angular-cli and demo api

    Install angular-cli with:
    ```
    $ npm i -g @angular/cli bookmonkey-api
    ```
4. IDE / Editor

    You should install an IDE or a text editor with JavaScript support. We recommend WebStorm as commercial option (https://www.jetbrains.com/webstorm/) or Visual Studio Code (https://code.visualstudio.com/) as free option.

5. Check your settings

Please run the following commands in the terminal:
```
$ node -v 
# => v8.0.0 (or higher)
$ npm -v
# => 6.0.0 (or higher)
$ ng --help
# => output of the angular-cli help
```

## Hints

Potential error sources
- update npm via npm -g i npm
- npm cache clear --force
If you have an old version of @angular/cli installed
```
npm unlink @angular/cli
npm rm -g @angular/cli
npm cache clear
```
