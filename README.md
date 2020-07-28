## Environment

```
$ sw_vers
ProductName:	Mac OS X
ProductVersion:	10.15.5
BuildVersion:	19F101

$ node -v
v12.18.3

$ npm -v
6.14.6

$ cat package.json
{
  "name": "my-razzle-app",
  "version": "0.1.0",
  "license": "MIT",
  "scripts": {
    "start": "razzle start",
    "build": "razzle build",
    "test": "razzle test --env=jsdom",
    "start:prod": "NODE_ENV=production node build/server.js"
  },
  "dependencies": {
    "express": "^4.17.1",
    "razzle": "^3.1.6",
    "react": "^16.13.1",
    "react-dom": "^16.13.1",
    "react-router-dom": "^5.2.0",
    "reset-css": "^5.0.1"
  }
}
```

## Steps to Recreate

```
$ npx create-razzle-app my-app
npx: installed 66 in 4.372s

Creating my-app...

> Success! Created files for "my-app" razzle app

  Installing npm modules:
    react
    react-dom
    react-router-dom
    razzle
    express

> Success! Installed dependencies for my-app

  Awesome! You're now ready to start coding.

  I already ran yarn for you, so your next steps are:
    cd my-app

  To start a local server for development:
    yarn start

  To build a version for production:
    yarn build

  To run the server in production:
    yarn start:prod

  Questions? Feedback? Please let me know!
  https://github.com/jaredpalmer/razzle/issues


$ cd my-app

$ npm start

> my-razzle-app@0.1.0 start /Users/christiannaths/Desktop/my-app
> razzle start

 WAIT  Compiling...


✔ Client
  Compiled successfully in 2.50s

✔ Server
  Compiled successfully in 335.56ms

✅  Server-side HMR Enabled!
🚀 started
^C

$ git init .
Initialized empty Git repository in /Users/christiannaths/Desktop/my-app/.git/

$ git add .

$ git commit -m "Creates new Razzle app"
[master (root-commit) 69810f0] Creates new Razzle app
 15 files changed, 9705 insertions(+)
 create mode 100644 .gitignore
 create mode 100644 README.md
 create mode 100644 package.json
 create mode 100644 public/favicon.ico
 create mode 100644 public/robots.txt
 create mode 100644 src/App.css
 create mode 100644 src/App.js
 create mode 100644 src/App.test.js
 create mode 100644 src/Home.css
 create mode 100644 src/Home.js
 create mode 100644 src/client.js
 create mode 100644 src/index.js
 create mode 100644 src/react.svg
 create mode 100644 src/server.js
 create mode 100644 yarn.lock

$ npm install --save reset-css
npm WARN deprecated fsevents@1.2.13: fsevents 1 will break on node v14+ and could be using insecure binaries. Upgrade to fsevents 2.
npm WARN deprecated left-pad@1.3.0: use String.prototype.padStart()
npm WARN deprecated request@2.88.2: request has been deprecated, see https://github.com/request/request/issues/3142
npm WARN deprecated request-promise-native@1.0.9: request-promise-native has been deprecated because it extends the now deprecated request package, see https://github.com/request/request/issues/3142
npm WARN deprecated assets-webpack-plugin@3.10.0: This version should have more strictly enforced the change to versions of node >10.x.x
npm WARN rm not removing /Users/christiannaths/Desktop/my-app/node_modules/.bin/jest as it wasn't installed by /Users/christiannaths/Desktop/my-app/node_modules/jest
npm WARN rm not removing /Users/christiannaths/Desktop/my-app/node_modules/.bin/semver as it wasn't installed by /Users/christiannaths/Desktop/my-app/node_modules/semver
npm WARN rm not removing /Users/christiannaths/Desktop/my-app/node_modules/.bin/mkdirp as it wasn't installed by /Users/christiannaths/Desktop/my-app/node_modules/mkdirp
npm WARN rm not removing /Users/christiannaths/Desktop/my-app/node_modules/.bin/json5 as it wasn't installed by /Users/christiannaths/Desktop/my-app/node_modules/json5

> fsevents@1.2.13 install /Users/christiannaths/Desktop/my-app/node_modules/fsevents
> node install.js

  SOLINK_MODULE(target) Release/.node
  CXX(target) Release/obj.target/fse/fsevents.o
  SOLINK_MODULE(target) Release/fse.node
npm notice created a lockfile as package-lock.json. You should commit this file.
npm WARN notsup Unsupported engine for watchpack-chokidar2@2.0.0: wanted: {"node":"<8.10.0"} (current: {"node":"12.18.3","npm":"6.14.6"})
npm WARN notsup Not compatible with your version of node/npm: watchpack-chokidar2@2.0.0
npm WARN my-razzle-app@0.1.0 No repository field.

+ reset-css@5.0.1
added 148 packages from 50 contributors, removed 75 packages, updated 1228 packages and audited 1380 packages in 70.659s

45 packages are looking for funding
  run `npm fund` for details

found 2 low severity vulnerabilities
  run `npm audit fix` to fix them, or `npm audit` for details

$ code .

$ npm start

> my-razzle-app@0.1.0 start /Users/christiannaths/Desktop/my-app
> razzle start

 WAIT  Compiling...


✔ Client
  Compiled successfully in 2.44s

✖ Server
  Compiled with some errors in 265.54ms

/Users/christiannaths/Desktop/my-app/node_modules/reset-css/reset.css:10
small, strike, strong, sub, sup, tt, var,
                                     ^^^

SyntaxError: Unexpected token 'var'
    at wrapSafe (internal/modules/cjs/loader.js:1053:16)
    at Module._compile (internal/modules/cjs/loader.js:1101:27)
    at Object.Module._extensions..js (internal/modules/cjs/loader.js:1157:10)
    at Module.load (internal/modules/cjs/loader.js:985:32)
    at Function.Module._load (internal/modules/cjs/loader.js:878:14)
    at Module.require (internal/modules/cjs/loader.js:1025:19)
    at require (internal/modules/cjs/helpers.js:72:18)
    at Object.reset-css (/Users/christiannaths/Desktop/my-app/external "reset-css":1:1)
    at __webpack_require__ (/Users/christiannaths/Desktop/my-app/build/webpack:/webpack/bootstrap:748:1)
    at fn (/Users/christiannaths/Desktop/my-app/build/webpack:/webpack/bootstrap:59:1)
```
