# 关于npm升级失败会把自己干掉这件事

2020.4.1	Whyer	macOS





日志：

```
~/Homepage/Shallow/Shallow-FrontEnd/Shallow-FrontEnd$ npm install -g npm
/usr/local/bin/npx -> /usr/local/lib/node_modules/npm/bin/npx-cli.js
/usr/local/bin/npm -> /usr/local/lib/node_modules/npm/bin/npm-cli.js
npm ERR! code EEXIST
npm ERR! syscall symlink
npm ERR! path ../../../lib/node_modules/npm/man/man1/npm-access.1
npm ERR! dest /usr/local/share/man/man1/npm-access.1
npm ERR! errno -17
npm ERR! EEXIST: file already exists, symlink '../../../lib/node_modules/npm/man/man1/npm-access.1' -> '/usr/local/share/man/man1/npm-access.1'
npm ERR! File exists: /usr/local/share/man/man1/npm-access.1
npm ERR! Remove the existing file and try again, or run npm
npm ERR! with --force to overwrite files recklessly.

npm ERR! A complete log of this run can be found in:
npm ERR!     /Users/yanghaowen/.npm/_logs/2020-04-01T15_24_29_478Z-debug.log
~/Homepage/Shallow/Shallow-FrontEnd/Shallow-FrontEnd$ npm i ajv
-bash: /usr/local/bin/npm: No such file or directory
~/Homepage/Shallow/Shallow-FrontEnd/Shallow-FrontEnd$ 
```

字面意思，文件已存在。

先修复一下npm：[抢救方法](./npm升级失败后的修复.md)

那就直接Override吧

```
/usr/local/share/man/man1$ sudo npm install npm@latest -g --force
npm WARN using --force I sure hope you know what you are doing.
/usr/local/bin/npm -> /usr/local/lib/node_modules/npm/bin/npm-cli.js
/usr/local/bin/npx -> /usr/local/lib/node_modules/npm/bin/npx-cli.js
+ npm@6.14.4
added 9 packages from 5 contributors, removed 4 packages and updated 29 packages in 4.954s
/usr/local/share/man/man1$ 
```

