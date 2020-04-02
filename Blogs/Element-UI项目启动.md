# 照着 Element-UI 教程，使用 Vue CLI 初始化工程的日志记录

2020.4.1	Whyer



日志：

```
~/Homepage/Shallow/Shallow-FrontEnd/Shallow-FrontEnd$ vue init webpack

? Generate project in current directory? Yes
? Project name shallow-fe
? Project description A Vue.js project
? Author Deslate <deslate@outlook.com>
? Vue build standalone
? Install vue-router? Yes
? Use ESLint to lint your code? Yes
? Pick an ESLint preset Standard
? Set up unit tests Yes
? Pick a test runner jest
? Setup e2e tests with Nightwatch? Yes
? Should we run `npm install` for you after the project has been created? (recom
mended) npm

   vue-cli · Generated "Shallow-FrontEnd".


# Installing project dependencies ...
# ========================

npm WARN deprecated extract-text-webpack-plugin@3.0.2: Deprecated. Please use https://github.com/webpack-contrib/mini-css-extract-plugin
npm WARN deprecated browserslist@2.11.3: Browserslist 2 could fail on reading Browserslist >3.0 config used in other tools.
npm WARN deprecated core-js@2.6.11: core-js@<3 is no longer maintained and not recommended for usage due to the number of issues. Please, upgrade your dependencies to the actual version of core-js@3.
npm WARN deprecated bfj-node4@5.3.1: Switch to the `bfj` package for fixes and new features!
npm WARN deprecated json3@3.3.2: Please use the native JSON object instead of JSON 3
npm WARN deprecated browserslist@1.7.7: Browserslist 2 could fail on reading Browserslist >3.0 config used in other tools.
npm WARN deprecated circular-json@0.3.3: CircularJSON is in maintenance only, flatted is its successor.
npm WARN deprecated socks@1.1.10: If using 2.x branch, please upgrade to at least 2.1.6 to avoid a serious bug with socket data flow and an import issue introduced in 2.1.0
npm WARN deprecated left-pad@1.3.0: use String.prototype.padStart()

> fsevents@1.2.12 install /Users/yanghaowen/Homepage/Shallow/Shallow-FrontEnd/Shallow-FrontEnd/node_modules/fsevents
> node-gyp rebuild

  SOLINK_MODULE(target) Release/.node
  CXX(target) Release/obj.target/fse/fsevents.o
  SOLINK_MODULE(target) Release/fse.node

> chromedriver@2.46.0 install /Users/yanghaowen/Homepage/Shallow/Shallow-FrontEnd/Shallow-FrontEnd/node_modules/chromedriver
> node install.js

Current existing ChromeDriver binary is unavailable, proceding with download and extraction.
Downloading from file:  https://chromedriver.storage.googleapis.com/2.46/chromedriver_mac64.zip
Saving to file: /var/folders/jz/1plm2f9x1ld10lk4k9cchf000000gn/T/2.46/chromedriver/chromedriver_mac64.zip
Received 781K...
Received 1566K...
Received 2348K...
Received 3129K...
Received 3910K...
Received 4692K...
Received 5473K...
Received 6254K...
Received 6891K total.
Extracting zip contents
Copying to target path /Users/yanghaowen/Homepage/Shallow/Shallow-FrontEnd/Shallow-FrontEnd/node_modules/chromedriver/lib/chromedriver
Fixing file permissions
Done. ChromeDriver binary available at /Users/yanghaowen/Homepage/Shallow/Shallow-FrontEnd/Shallow-FrontEnd/node_modules/chromedriver/lib/chromedriver/chromedriver

> core-js@2.6.11 postinstall /Users/yanghaowen/Homepage/Shallow/Shallow-FrontEnd/Shallow-FrontEnd/node_modules/core-js
> node -e "try{require('./postinstall')}catch(e){}"

Thank you for using core-js ( https://github.com/zloirock/core-js ) for polyfilling JavaScript standard library!

The project needs your help! Please consider supporting of core-js on Open Collective or Patreon: 
> https://opencollective.com/core-js 
> https://www.patreon.com/zloirock 

Also, the author of core-js ( https://github.com/zloirock ) is looking for a good job -)


> uglifyjs-webpack-plugin@0.4.6 postinstall /Users/yanghaowen/Homepage/Shallow/Shallow-FrontEnd/Shallow-FrontEnd/node_modules/webpack/node_modules/uglifyjs-webpack-plugin
> node lib/post_install.js

npm notice created a lockfile as package-lock.json. You should commit this file.
npm WARN ajv-keywords@2.1.1 requires a peer of ajv@^5.0.0 but none is installed. You must install peer dependencies yourself.

added 1826 packages from 1118 contributors in 604.302s

28 packages are looking for funding
  run `npm fund` for details



Running eslint --fix to comply with chosen preset rules...
# ========================


> shallow-fe@1.0.0 lint /Users/yanghaowen/Homepage/Shallow/Shallow-FrontEnd/Shallow-FrontEnd
> eslint --ext .js,.vue src test/unit test/e2e/specs "--fix"


# Project initialization finished!
# ========================

To get started:

  npm run dev
  
Documentation can be found at https://vuejs-templates.github.io/webpack


~/Homepage/Shallow/Shallow-FrontEnd/Shallow-FrontEnd$ npm i && npm i element-ui
npm WARN ajv-keywords@2.1.1 requires a peer of ajv@^5.0.0 but none is installed. You must install peer dependencies yourself.

up to date in 6.163s

28 packages are looking for funding
  run `npm fund` for details

npm WARN ajv-keywords@2.1.1 requires a peer of ajv@^5.0.0 but none is installed. You must install peer dependencies yourself.

+ element-ui@2.13.0
added 6 packages from 6 contributors in 6.048s

28 packages are looking for funding
  run `npm fund` for details
```

