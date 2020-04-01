# npm 修复

今天更新npm 结果更新失败了

```
~$ sudo npm install npm@latest -g
Password:
/usr/local/bin/npm -> /usr/local/lib/node_modules/npm/bin/npm-cli.js
/usr/local/bin/npx -> /usr/local/lib/node_modules/npm/bin/npx-cli.js
npm ERR! code EEXIST
npm ERR! syscall symlink
npm ERR! path ../../../lib/node_modules/npm/man/man1/npm-adduser.1
npm ERR! dest /usr/local/share/man/man1/npm-adduser.1
npm ERR! errno -17
npm ERR! EEXIST: file already exists, symlink '../../../lib/node_modules/npm/man/man1/npm-adduser.1' -> '/usr/local/share/man/man1/npm-adduser.1'
npm ERR! File exists: /usr/local/share/man/man1/npm-adduser.1
npm ERR! Remove the existing file and try again, or run npm
npm ERR! with --force to overwrite files recklessly.

npm ERR! A complete log of this run can be found in:
npm ERR!     /Users/yanghaowen/.npm/_logs/2020-04-01T11_43_14_419Z-debug.log
~$ sudo npm install npm@latest -g
sudo: npm: command not found
~$ sudo npm install npm@latest -g
sudo: npm: command not found
~$ npm install npm@latest -g
-bash: /usr/local/bin/npm: No such file or directory
```

好现在就只能重装了。

如果windows，请参考官网给出的方法：https://www.npmjs.cn/troubleshooting/if-your-npm-is-broken/



我用的是mac自带的包管理工具 homebrew

```
~$ brew uninstall node
Uninstalling /usr/local/Cellar/node/13.4.0... (4,663 files, 59MB)
~$ brew install node
Updating Homebrew...
^C==> Downloading https://homebrew.bintray.com/bottles/node-13.4.0.catalina.bottle
Already downloaded: /Users/yanghaowen/Library/Caches/Homebrew/downloads/233153271c2e474e950dc4e605b3b3043c64c9d55bf990280fdf2240f23c62d7--node-13.4.0.catalina.bottle.tar.gz
==> Pouring node-13.4.0.catalina.bottle.tar.gz
Error: The `brew link` step did not complete successfully
The formula built, but is not symlinked into /usr/local
Could not symlink bin/node
Target /usr/local/bin/node
already exists. You may want to remove it:
  rm '/usr/local/bin/node'

To force the link and overwrite all conflicting files:
  brew link --overwrite node

To list all files that would be deleted:
  brew link --overwrite --dry-run node

Possible conflicting files are:
/usr/local/bin/node
/usr/local/include/node/common.gypi
/usr/local/include/node/config.gypi
/usr/local/include/node/js_native_api.h
/usr/local/include/node/js_native_api_types.h
/usr/local/include/node/libplatform/libplatform-export.h
/usr/local/include/node/libplatform/libplatform.h
/usr/local/include/node/libplatform/v8-tracing.h
/usr/local/include/node/node.h
/usr/local/include/node/node_api.h
/usr/local/include/node/node_api_types.h
/usr/local/include/node/node_buffer.h
/usr/local/include/node/node_object_wrap.h
/usr/local/include/node/node_version.h
/usr/local/include/node/openssl/aes.h
/usr/local/include/node/openssl/archs/BSD-x86/asm/crypto/buildinf.h
/usr/local/include/node/openssl/archs/BSD-x86/asm/crypto/include/internal/bn_conf.h
/usr/local/include/node/openssl/archs/BSD-x86/asm/crypto/include/internal/dso_conf.h
/usr/local/include/node/openssl/archs/BSD-x86/asm/include/openssl/opensslconf.h
/usr/local/include/node/openssl/archs/BSD-x86/asm/include/progs.h
/usr/local/include/node/openssl/archs/BSD-x86/asm_avx2/crypto/buildinf.h
/usr/local/include/node/openssl/archs/BSD-x86/asm_avx2/crypto/include/internal/bn_conf.h
/usr/local/include/node/openssl/archs/BSD-x86/asm_avx2/crypto/include/internal/dso_conf.h
/usr/local/include/node/openssl/archs/BSD-x86/asm_avx2/include/openssl/opensslconf.h
/usr/local/include/node/openssl/archs/BSD-x86/asm_avx2/include/progs.h
/usr/local/include/node/openssl/archs/BSD-x86/no-asm/crypto/buildinf.h
/usr/local/include/node/openssl/archs/BSD-x86/no-asm/crypto/include/internal/bn_conf.h
/usr/local/include/node/openssl/archs/BSD-x86/no-asm/crypto/include/internal/dso_conf.h
/usr/local/include/node/openssl/archs/BSD-x86/no-asm/include/openssl/opensslconf.h
/usr/local/include/node/openssl/archs/BSD-x86/no-asm/include/progs.h
/usr/local/include/node/openssl/archs/BSD-x86_64/asm/crypto/buildinf.h
/usr/local/include/node/openssl/archs/BSD-x86_64/asm/crypto/include/internal/bn_conf.h
/usr/local/include/node/openssl/archs/BSD-x86_64/asm/crypto/include/internal/dso_conf.h
/usr/local/include/node/openssl/archs/BSD-x86_64/asm/include/openssl/opensslconf.h
/usr/local/include/node/openssl/archs/BSD-x86_64/asm/include/progs.h
/usr/local/include/node/openssl/archs/BSD-x86_64/asm_avx2/crypto/buildinf.h
/usr/local/include/node/openssl/archs/BSD-x86_64/asm_avx2/crypto/include/internal/bn_conf.h
/usr/local/include/node/openssl/archs/BSD-x86_64/asm_avx2/crypto/include/internal/dso_conf.h
/usr/local/include/node/openssl/archs/BSD-x86_64/asm_avx2/include/openssl/opensslconf.h
/usr/local/include/node/openssl/archs/BSD-x86_64/asm_avx2/include/progs.h
/usr/local/include/node/openssl/archs/BSD-x86_64/no-asm/crypto/buildinf.h
/usr/local/include/node/openssl/archs/BSD-x86_64/no-asm/crypto/include/internal/bn_conf.h
/usr/local/include/node/openssl/archs/BSD-x86_64/no-asm/crypto/include/internal/dso_conf.h
/usr/local/include/node/openssl/archs/BSD-x86_64/no-asm/include/openssl/opensslconf.h
/usr/local/include/node/openssl/archs/BSD-x86_64/no-asm/include/progs.h
/usr/local/include/node/openssl/archs/VC-WIN32/asm/crypto/buildinf.h
/usr/local/include/node/openssl/archs/VC-WIN32/asm/crypto/include/internal/bn_conf.h
/usr/local/include/node/openssl/archs/VC-WIN32/asm/crypto/include/internal/dso_conf.h
/usr/local/include/node/openssl/archs/VC-WIN32/asm/include/openssl/opensslconf.h
/usr/local/include/node/openssl/archs/VC-WIN32/asm/include/progs.h
/usr/local/include/node/openssl/archs/VC-WIN32/asm_avx2/crypto/buildinf.h
/usr/local/include/node/openssl/archs/VC-WIN32/asm_avx2/crypto/include/internal/bn_conf.h
/usr/local/include/node/openssl/archs/VC-WIN32/asm_avx2/crypto/include/internal/dso_conf.h
/usr/local/include/node/openssl/archs/VC-WIN32/asm_avx2/include/openssl/opensslconf.h
/usr/local/include/node/openssl/archs/VC-WIN32/asm_avx2/include/progs.h
/usr/local/include/node/openssl/archs/VC-WIN32/no-asm/crypto/buildinf.h
/usr/local/include/node/openssl/archs/VC-WIN32/no-asm/crypto/include/internal/bn_conf.h
/usr/local/include/node/openssl/archs/VC-WIN32/no-asm/crypto/include/internal/dso_conf.h
/usr/local/include/node/openssl/archs/VC-WIN32/no-asm/include/openssl/opensslconf.h
/usr/local/include/node/openssl/archs/VC-WIN32/no-asm/include/progs.h
/usr/local/include/node/openssl/archs/VC-WIN64-ARM/no-asm/crypto/buildinf.h
/usr/local/include/node/openssl/archs/VC-WIN64-ARM/no-asm/crypto/include/internal/bn_conf.h
/usr/local/include/node/openssl/archs/VC-WIN64-ARM/no-asm/crypto/include/internal/dso_conf.h
/usr/local/include/node/openssl/archs/VC-WIN64-ARM/no-asm/include/openssl/opensslconf.h
/usr/local/include/node/openssl/archs/VC-WIN64-ARM/no-asm/include/progs.h
/usr/local/include/node/openssl/archs/VC-WIN64A/asm/crypto/buildinf.h
/usr/local/include/node/openssl/archs/VC-WIN64A/asm/crypto/include/internal/bn_conf.h
/usr/local/include/node/openssl/archs/VC-WIN64A/asm/crypto/include/internal/dso_conf.h
/usr/local/include/node/openssl/archs/VC-WIN64A/asm/include/openssl/opensslconf.h
/usr/local/include/node/openssl/archs/VC-WIN64A/asm/include/progs.h
/usr/local/include/node/openssl/archs/VC-WIN64A/asm_avx2/crypto/buildinf.h
/usr/local/include/node/openssl/archs/VC-WIN64A/asm_avx2/crypto/include/internal/bn_conf.h
/usr/local/include/node/openssl/archs/VC-WIN64A/asm_avx2/crypto/include/internal/dso_conf.h
/usr/local/include/node/openssl/archs/VC-WIN64A/asm_avx2/include/openssl/opensslconf.h
/usr/local/include/node/openssl/archs/VC-WIN64A/asm_avx2/include/progs.h
/usr/local/include/node/openssl/archs/VC-WIN64A/no-asm/crypto/buildinf.h
/usr/local/include/node/openssl/archs/VC-WIN64A/no-asm/crypto/include/internal/bn_conf.h
/usr/local/include/node/openssl/archs/VC-WIN64A/no-asm/crypto/include/internal/dso_conf.h
/usr/local/include/node/openssl/archs/VC-WIN64A/no-asm/include/openssl/opensslconf.h
/usr/local/include/node/openssl/archs/VC-WIN64A/no-asm/include/progs.h
/usr/local/include/node/openssl/archs/aix-gcc/asm/crypto/buildinf.h
/usr/local/include/node/openssl/archs/aix-gcc/asm/crypto/include/internal/bn_conf.h
/usr/local/include/node/openssl/archs/aix-gcc/asm/crypto/include/internal/dso_conf.h
/usr/local/include/node/openssl/archs/aix-gcc/asm/include/openssl/opensslconf.h
/usr/local/include/node/openssl/archs/aix-gcc/asm/include/progs.h
/usr/local/include/node/openssl/archs/aix-gcc/asm_avx2/crypto/buildinf.h
/usr/local/include/node/openssl/archs/aix-gcc/asm_avx2/crypto/include/internal/bn_conf.h
/usr/local/include/node/openssl/archs/aix-gcc/asm_avx2/crypto/include/internal/dso_conf.h
/usr/local/include/node/openssl/archs/aix-gcc/asm_avx2/include/openssl/opensslconf.h
/usr/local/include/node/openssl/archs/aix-gcc/asm_avx2/include/progs.h
/usr/local/include/node/openssl/archs/aix-gcc/no-asm/crypto/buildinf.h
/usr/local/include/node/openssl/archs/aix-gcc/no-asm/crypto/include/internal/bn_conf.h
/usr/local/include/node/openssl/archs/aix-gcc/no-asm/crypto/include/internal/dso_conf.h
/usr/local/include/node/openssl/archs/aix-gcc/no-asm/include/openssl/opensslconf.h
/usr/local/include/node/openssl/archs/aix-gcc/no-asm/include/progs.h
/usr/local/include/node/openssl/archs/aix64-gcc/asm/crypto/buildinf.h
/usr/local/include/node/openssl/archs/aix64-gcc/asm/crypto/include/internal/bn_conf.h
/usr/local/include/node/openssl/archs/aix64-gcc/asm/crypto/include/internal/dso_conf.h
/usr/local/include/node/openssl/archs/aix64-gcc/asm/include/openssl/opensslconf.h
/usr/local/include/node/openssl/archs/aix64-gcc/asm/include/progs.h
/usr/local/include/node/openssl/archs/aix64-gcc/asm_avx2/crypto/buildinf.h
/usr/local/include/node/openssl/archs/aix64-gcc/asm_avx2/crypto/include/internal/bn_conf.h
/usr/local/include/node/openssl/archs/aix64-gcc/asm_avx2/crypto/include/internal/dso_conf.h
/usr/local/include/node/openssl/archs/aix64-gcc/asm_avx2/include/openssl/opensslconf.h
/usr/local/include/node/openssl/archs/aix64-gcc/asm_avx2/include/progs.h
/usr/local/include/node/openssl/archs/aix64-gcc/no-asm/crypto/buildinf.h
/usr/local/include/node/openssl/archs/aix64-gcc/no-asm/crypto/include/internal/bn_conf.h
/usr/local/include/node/openssl/archs/aix64-gcc/no-asm/crypto/include/internal/dso_conf.h
/usr/local/include/node/openssl/archs/aix64-gcc/no-asm/include/openssl/opensslconf.h
/usr/local/include/node/openssl/archs/aix64-gcc/no-asm/include/progs.h
/usr/local/include/node/openssl/archs/darwin-i386-cc/asm/crypto/buildinf.h
/usr/local/include/node/openssl/archs/darwin-i386-cc/asm/crypto/include/internal/bn_conf.h
/usr/local/include/node/openssl/archs/darwin-i386-cc/asm/crypto/include/internal/dso_conf.h
/usr/local/include/node/openssl/archs/darwin-i386-cc/asm/include/openssl/opensslconf.h
/usr/local/include/node/openssl/archs/darwin-i386-cc/asm/include/progs.h
/usr/local/include/node/openssl/archs/darwin-i386-cc/asm_avx2/crypto/buildinf.h
/usr/local/include/node/openssl/archs/darwin-i386-cc/asm_avx2/crypto/include/internal/bn_conf.h
/usr/local/include/node/openssl/archs/darwin-i386-cc/asm_avx2/crypto/include/internal/dso_conf.h
/usr/local/include/node/openssl/archs/darwin-i386-cc/asm_avx2/include/openssl/opensslconf.h
/usr/local/include/node/openssl/archs/darwin-i386-cc/asm_avx2/include/progs.h
/usr/local/include/node/openssl/archs/darwin-i386-cc/no-asm/crypto/buildinf.h
/usr/local/include/node/openssl/archs/darwin-i386-cc/no-asm/crypto/include/internal/bn_conf.h
/usr/local/include/node/openssl/archs/darwin-i386-cc/no-asm/crypto/include/internal/dso_conf.h
/usr/local/include/node/openssl/archs/darwin-i386-cc/no-asm/include/openssl/opensslconf.h
/usr/local/include/node/openssl/archs/darwin-i386-cc/no-asm/include/progs.h
/usr/local/include/node/openssl/archs/darwin64-x86_64-cc/asm/crypto/buildinf.h
/usr/local/include/node/openssl/archs/darwin64-x86_64-cc/asm/crypto/include/internal/bn_conf.h
/usr/local/include/node/openssl/archs/darwin64-x86_64-cc/asm/crypto/include/internal/dso_conf.h
/usr/local/include/node/openssl/archs/darwin64-x86_64-cc/asm/include/openssl/opensslconf.h
/usr/local/include/node/openssl/archs/darwin64-x86_64-cc/asm/include/progs.h
/usr/local/include/node/openssl/archs/darwin64-x86_64-cc/asm_avx2/crypto/buildinf.h
/usr/local/include/node/openssl/archs/darwin64-x86_64-cc/asm_avx2/crypto/include/internal/bn_conf.h
/usr/local/include/node/openssl/archs/darwin64-x86_64-cc/asm_avx2/crypto/include/internal/dso_conf.h
/usr/local/include/node/openssl/archs/darwin64-x86_64-cc/asm_avx2/include/openssl/opensslconf.h
/usr/local/include/node/openssl/archs/darwin64-x86_64-cc/asm_avx2/include/progs.h
/usr/local/include/node/openssl/archs/darwin64-x86_64-cc/no-asm/crypto/buildinf.h
/usr/local/include/node/openssl/archs/darwin64-x86_64-cc/no-asm/crypto/include/internal/bn_conf.h
/usr/local/include/node/openssl/archs/darwin64-x86_64-cc/no-asm/crypto/include/internal/dso_conf.h
/usr/local/include/node/openssl/archs/darwin64-x86_64-cc/no-asm/include/openssl/opensslconf.h
/usr/local/include/node/openssl/archs/darwin64-x86_64-cc/no-asm/include/progs.h
/usr/local/include/node/openssl/archs/linux-aarch64/asm/crypto/buildinf.h
/usr/local/include/node/openssl/archs/linux-aarch64/asm/crypto/include/internal/bn_conf.h
/usr/local/include/node/openssl/archs/linux-aarch64/asm/crypto/include/internal/dso_conf.h
/usr/local/include/node/openssl/archs/linux-aarch64/asm/include/openssl/opensslconf.h
/usr/local/include/node/openssl/archs/linux-aarch64/asm/include/progs.h
/usr/local/include/node/openssl/archs/linux-aarch64/asm_avx2/crypto/buildinf.h
/usr/local/include/node/openssl/archs/linux-aarch64/asm_avx2/crypto/include/internal/bn_conf.h
/usr/local/include/node/openssl/archs/linux-aarch64/asm_avx2/crypto/include/internal/dso_conf.h
/usr/local/include/node/openssl/archs/linux-aarch64/asm_avx2/include/openssl/opensslconf.h
/usr/local/include/node/openssl/archs/linux-aarch64/asm_avx2/include/progs.h
/usr/local/include/node/openssl/archs/linux-aarch64/no-asm/crypto/buildinf.h
/usr/local/include/node/openssl/archs/linux-aarch64/no-asm/crypto/include/internal/bn_conf.h
/usr/local/include/node/openssl/archs/linux-aarch64/no-asm/crypto/include/internal/dso_conf.h
/usr/local/include/node/openssl/archs/linux-aarch64/no-asm/include/openssl/opensslconf.h
/usr/local/include/node/openssl/archs/linux-aarch64/no-asm/include/progs.h
/usr/local/include/node/openssl/archs/linux-armv4/asm/crypto/buildinf.h
/usr/local/include/node/openssl/archs/linux-armv4/asm/crypto/include/internal/bn_conf.h
/usr/local/include/node/openssl/archs/linux-armv4/asm/crypto/include/internal/dso_conf.h
/usr/local/include/node/openssl/archs/linux-armv4/asm/include/openssl/opensslconf.h
/usr/local/include/node/openssl/archs/linux-armv4/asm/include/progs.h
/usr/local/include/node/openssl/archs/linux-armv4/asm_avx2/crypto/buildinf.h
/usr/local/include/node/openssl/archs/linux-armv4/asm_avx2/crypto/include/internal/bn_conf.h
/usr/local/include/node/openssl/archs/linux-armv4/asm_avx2/crypto/include/internal/dso_conf.h
/usr/local/include/node/openssl/archs/linux-armv4/asm_avx2/include/openssl/opensslconf.h
/usr/local/include/node/openssl/archs/linux-armv4/asm_avx2/include/progs.h
/usr/local/include/node/openssl/archs/linux-armv4/no-asm/crypto/buildinf.h
/usr/local/include/node/openssl/archs/linux-armv4/no-asm/crypto/include/internal/bn_conf.h
/usr/local/include/node/openssl/archs/linux-armv4/no-asm/crypto/include/internal/dso_conf.h
/usr/local/include/node/openssl/archs/linux-armv4/no-asm/include/openssl/opensslconf.h
/usr/local/include/node/openssl/archs/linux-armv4/no-asm/include/progs.h
/usr/local/include/node/openssl/archs/linux-elf/asm/crypto/buildinf.h
/usr/local/include/node/openssl/archs/linux-elf/asm/crypto/include/internal/bn_conf.h
/usr/local/include/node/openssl/archs/linux-elf/asm/crypto/include/internal/dso_conf.h
/usr/local/include/node/openssl/archs/linux-elf/asm/include/openssl/opensslconf.h
/usr/local/include/node/openssl/archs/linux-elf/asm/include/progs.h
/usr/local/include/node/openssl/archs/linux-elf/asm_avx2/crypto/buildinf.h
/usr/local/include/node/openssl/archs/linux-elf/asm_avx2/crypto/include/internal/bn_conf.h
/usr/local/include/node/openssl/archs/linux-elf/asm_avx2/crypto/include/internal/dso_conf.h
/usr/local/include/node/openssl/archs/linux-elf/asm_avx2/include/openssl/opensslconf.h
/usr/local/include/node/openssl/archs/linux-elf/asm_avx2/include/progs.h
/usr/local/include/node/openssl/archs/linux-elf/no-asm/crypto/buildinf.h
/usr/local/include/node/openssl/archs/linux-elf/no-asm/crypto/include/internal/bn_conf.h
/usr/local/include/node/openssl/archs/linux-elf/no-asm/crypto/include/internal/dso_conf.h
/usr/local/include/node/openssl/archs/linux-elf/no-asm/include/openssl/opensslconf.h
/usr/local/include/node/openssl/archs/linux-elf/no-asm/include/progs.h
/usr/local/include/node/openssl/archs/linux-ppc/asm/crypto/buildinf.h
/usr/local/include/node/openssl/archs/linux-ppc/asm/crypto/include/internal/bn_conf.h
/usr/local/include/node/openssl/archs/linux-ppc/asm/crypto/include/internal/dso_conf.h
/usr/local/include/node/openssl/archs/linux-ppc/asm/include/openssl/opensslconf.h
/usr/local/include/node/openssl/archs/linux-ppc/asm/include/progs.h
/usr/local/include/node/openssl/archs/linux-ppc/asm_avx2/crypto/buildinf.h
/usr/local/include/node/openssl/archs/linux-ppc/asm_avx2/crypto/include/internal/bn_conf.h
/usr/local/include/node/openssl/archs/linux-ppc/asm_avx2/crypto/include/internal/dso_conf.h
/usr/local/include/node/openssl/archs/linux-ppc/asm_avx2/include/openssl/opensslconf.h
/usr/local/include/node/openssl/archs/linux-ppc/asm_avx2/include/progs.h
/usr/local/include/node/openssl/archs/linux-ppc/no-asm/crypto/buildinf.h
/usr/local/include/node/openssl/archs/linux-ppc/no-asm/crypto/include/internal/bn_conf.h
/usr/local/include/node/openssl/archs/linux-ppc/no-asm/crypto/include/internal/dso_conf.h
/usr/local/include/node/openssl/archs/linux-ppc/no-asm/include/openssl/opensslconf.h
/usr/local/include/node/openssl/archs/linux-ppc/no-asm/include/progs.h
/usr/local/include/node/openssl/archs/linux-ppc64/asm/crypto/buildinf.h
/usr/local/include/node/openssl/archs/linux-ppc64/asm/crypto/include/internal/bn_conf.h
/usr/local/include/node/openssl/archs/linux-ppc64/asm/crypto/include/internal/dso_conf.h
/usr/local/include/node/openssl/archs/linux-ppc64/asm/include/openssl/opensslconf.h
/usr/local/include/node/openssl/archs/linux-ppc64/asm/include/progs.h
/usr/local/include/node/openssl/archs/linux-ppc64/asm_avx2/crypto/buildinf.h
/usr/local/include/node/openssl/archs/linux-ppc64/asm_avx2/crypto/include/internal/bn_conf.h
/usr/local/include/node/openssl/archs/linux-ppc64/asm_avx2/crypto/include/internal/dso_conf.h
/usr/local/include/node/openssl/archs/linux-ppc64/asm_avx2/include/openssl/opensslconf.h
/usr/local/include/node/openssl/archs/linux-ppc64/asm_avx2/include/progs.h
/usr/local/include/node/openssl/archs/linux-ppc64/no-asm/crypto/buildinf.h
/usr/local/include/node/openssl/archs/linux-ppc64/no-asm/crypto/include/internal/bn_conf.h
/usr/local/include/node/openssl/archs/linux-ppc64/no-asm/crypto/include/internal/dso_conf.h
/usr/local/include/node/openssl/archs/linux-ppc64/no-asm/include/openssl/opensslconf.h
/usr/local/include/node/openssl/archs/linux-ppc64/no-asm/include/progs.h
/usr/local/include/node/openssl/archs/linux-ppc64le/asm/crypto/buildinf.h
/usr/local/include/node/openssl/archs/linux-ppc64le/asm/crypto/include/internal/bn_conf.h
/usr/local/include/node/openssl/archs/linux-ppc64le/asm/crypto/include/internal/dso_conf.h
/usr/local/include/node/openssl/archs/linux-ppc64le/asm/include/openssl/opensslconf.h
/usr/local/include/node/openssl/archs/linux-ppc64le/asm/include/progs.h
/usr/local/include/node/openssl/archs/linux-ppc64le/asm_avx2/crypto/buildinf.h
/usr/local/include/node/openssl/archs/linux-ppc64le/asm_avx2/crypto/include/internal/bn_conf.h
/usr/local/include/node/openssl/archs/linux-ppc64le/asm_avx2/crypto/include/internal/dso_conf.h
/usr/local/include/node/openssl/archs/linux-ppc64le/asm_avx2/include/openssl/opensslconf.h
/usr/local/include/node/openssl/archs/linux-ppc64le/asm_avx2/include/progs.h
/usr/local/include/node/openssl/archs/linux-ppc64le/no-asm/crypto/buildinf.h
/usr/local/include/node/openssl/archs/linux-ppc64le/no-asm/crypto/include/internal/bn_conf.h
/usr/local/include/node/openssl/archs/linux-ppc64le/no-asm/crypto/include/internal/dso_conf.h
/usr/local/include/node/openssl/archs/linux-ppc64le/no-asm/include/openssl/opensslconf.h
/usr/local/include/node/openssl/archs/linux-ppc64le/no-asm/include/progs.h
/usr/local/include/node/openssl/archs/linux-x32/asm/crypto/buildinf.h
/usr/local/include/node/openssl/archs/linux-x32/asm/crypto/include/internal/bn_conf.h
/usr/local/include/node/openssl/archs/linux-x32/asm/crypto/include/internal/dso_conf.h
/usr/local/include/node/openssl/archs/linux-x32/asm/include/openssl/opensslconf.h
/usr/local/include/node/openssl/archs/linux-x32/asm/include/progs.h
/usr/local/include/node/openssl/archs/linux-x32/asm_avx2/crypto/buildinf.h
/usr/local/include/node/openssl/archs/linux-x32/asm_avx2/crypto/include/internal/bn_conf.h
/usr/local/include/node/openssl/archs/linux-x32/asm_avx2/crypto/include/internal/dso_conf.h
/usr/local/include/node/openssl/archs/linux-x32/asm_avx2/include/openssl/opensslconf.h
/usr/local/include/node/openssl/archs/linux-x32/asm_avx2/include/progs.h
/usr/local/include/node/openssl/archs/linux-x32/no-asm/crypto/buildinf.h
/usr/local/include/node/openssl/archs/linux-x32/no-asm/crypto/include/internal/bn_conf.h
/usr/local/include/node/openssl/archs/linux-x32/no-asm/crypto/include/internal/dso_conf.h
/usr/local/include/node/openssl/archs/linux-x32/no-asm/include/openssl/opensslconf.h
/usr/local/include/node/openssl/archs/linux-x32/no-asm/include/progs.h
/usr/local/include/node/openssl/archs/linux-x86_64/asm/crypto/buildinf.h
/usr/local/include/node/openssl/archs/linux-x86_64/asm/crypto/include/internal/bn_conf.h
/usr/local/include/node/openssl/archs/linux-x86_64/asm/crypto/include/internal/dso_conf.h
/usr/local/include/node/openssl/archs/linux-x86_64/asm/include/openssl/opensslconf.h
/usr/local/include/node/openssl/archs/linux-x86_64/asm/include/progs.h
/usr/local/include/node/openssl/archs/linux-x86_64/asm_avx2/crypto/buildinf.h
/usr/local/include/node/openssl/archs/linux-x86_64/asm_avx2/crypto/include/internal/bn_conf.h
/usr/local/include/node/openssl/archs/linux-x86_64/asm_avx2/crypto/include/internal/dso_conf.h
/usr/local/include/node/openssl/archs/linux-x86_64/asm_avx2/include/openssl/opensslconf.h
/usr/local/include/node/openssl/archs/linux-x86_64/asm_avx2/include/progs.h
/usr/local/include/node/openssl/archs/linux-x86_64/no-asm/crypto/buildinf.h
/usr/local/include/node/openssl/archs/linux-x86_64/no-asm/crypto/include/internal/bn_conf.h
/usr/local/include/node/openssl/archs/linux-x86_64/no-asm/crypto/include/internal/dso_conf.h
/usr/local/include/node/openssl/archs/linux-x86_64/no-asm/include/openssl/opensslconf.h
/usr/local/include/node/openssl/archs/linux-x86_64/no-asm/include/progs.h
/usr/local/include/node/openssl/archs/linux32-s390x/asm/crypto/buildinf.h
/usr/local/include/node/openssl/archs/linux32-s390x/asm/crypto/include/internal/bn_conf.h
/usr/local/include/node/openssl/archs/linux32-s390x/asm/crypto/include/internal/dso_conf.h
/usr/local/include/node/openssl/archs/linux32-s390x/asm/include/openssl/opensslconf.h
/usr/local/include/node/openssl/archs/linux32-s390x/asm/include/progs.h
/usr/local/include/node/openssl/archs/linux32-s390x/asm_avx2/crypto/buildinf.h
/usr/local/include/node/openssl/archs/linux32-s390x/asm_avx2/crypto/include/internal/bn_conf.h
/usr/local/include/node/openssl/archs/linux32-s390x/asm_avx2/crypto/include/internal/dso_conf.h
/usr/local/include/node/openssl/archs/linux32-s390x/asm_avx2/include/openssl/opensslconf.h
/usr/local/include/node/openssl/archs/linux32-s390x/asm_avx2/include/progs.h
/usr/local/include/node/openssl/archs/linux32-s390x/no-asm/crypto/buildinf.h
/usr/local/include/node/openssl/archs/linux32-s390x/no-asm/crypto/include/internal/bn_conf.h
/usr/local/include/node/openssl/archs/linux32-s390x/no-asm/crypto/include/internal/dso_conf.h
/usr/local/include/node/openssl/archs/linux32-s390x/no-asm/include/openssl/opensslconf.h
/usr/local/include/node/openssl/archs/linux32-s390x/no-asm/include/progs.h
/usr/local/include/node/openssl/archs/linux64-mips64/asm/crypto/buildinf.h
/usr/local/include/node/openssl/archs/linux64-mips64/asm/crypto/include/internal/bn_conf.h
/usr/local/include/node/openssl/archs/linux64-mips64/asm/crypto/include/internal/dso_conf.h
/usr/local/include/node/openssl/archs/linux64-mips64/asm/include/openssl/opensslconf.h
/usr/local/include/node/openssl/archs/linux64-mips64/asm/include/progs.h
/usr/local/include/node/openssl/archs/linux64-mips64/asm_avx2/crypto/buildinf.h
/usr/local/include/node/openssl/archs/linux64-mips64/asm_avx2/crypto/include/internal/bn_conf.h
/usr/local/include/node/openssl/archs/linux64-mips64/asm_avx2/crypto/include/internal/dso_conf.h
/usr/local/include/node/openssl/archs/linux64-mips64/asm_avx2/include/openssl/opensslconf.h
/usr/local/include/node/openssl/archs/linux64-mips64/asm_avx2/include/progs.h
/usr/local/include/node/openssl/archs/linux64-mips64/no-asm/crypto/buildinf.h
/usr/local/include/node/openssl/archs/linux64-mips64/no-asm/crypto/include/internal/bn_conf.h
/usr/local/include/node/openssl/archs/linux64-mips64/no-asm/crypto/include/internal/dso_conf.h
/usr/local/include/node/openssl/archs/linux64-mips64/no-asm/include/openssl/opensslconf.h
/usr/local/include/node/openssl/archs/linux64-mips64/no-asm/include/progs.h
/usr/local/include/node/openssl/archs/linux64-s390x/asm/crypto/buildinf.h
/usr/local/include/node/openssl/archs/linux64-s390x/asm/crypto/include/internal/bn_conf.h
/usr/local/include/node/openssl/archs/linux64-s390x/asm/crypto/include/internal/dso_conf.h
/usr/local/include/node/openssl/archs/linux64-s390x/asm/include/openssl/opensslconf.h
/usr/local/include/node/openssl/archs/linux64-s390x/asm/include/progs.h
/usr/local/include/node/openssl/archs/linux64-s390x/asm_avx2/crypto/buildinf.h
/usr/local/include/node/openssl/archs/linux64-s390x/asm_avx2/crypto/include/internal/bn_conf.h
/usr/local/include/node/openssl/archs/linux64-s390x/asm_avx2/crypto/include/internal/dso_conf.h
/usr/local/include/node/openssl/archs/linux64-s390x/asm_avx2/include/openssl/opensslconf.h
/usr/local/include/node/openssl/archs/linux64-s390x/asm_avx2/include/progs.h
/usr/local/include/node/openssl/archs/linux64-s390x/no-asm/crypto/buildinf.h
/usr/local/include/node/openssl/archs/linux64-s390x/no-asm/crypto/include/internal/bn_conf.h
/usr/local/include/node/openssl/archs/linux64-s390x/no-asm/crypto/include/internal/dso_conf.h
/usr/local/include/node/openssl/archs/linux64-s390x/no-asm/include/openssl/opensslconf.h
/usr/local/include/node/openssl/archs/linux64-s390x/no-asm/include/progs.h
/usr/local/include/node/openssl/archs/solaris-x86-gcc/asm/crypto/buildinf.h
/usr/local/include/node/openssl/archs/solaris-x86-gcc/asm/crypto/include/internal/bn_conf.h
/usr/local/include/node/openssl/archs/solaris-x86-gcc/asm/crypto/include/internal/dso_conf.h
/usr/local/include/node/openssl/archs/solaris-x86-gcc/asm/include/openssl/opensslconf.h
/usr/local/include/node/openssl/archs/solaris-x86-gcc/asm/include/progs.h
/usr/local/include/node/openssl/archs/solaris-x86-gcc/asm_avx2/crypto/buildinf.h
/usr/local/include/node/openssl/archs/solaris-x86-gcc/asm_avx2/crypto/include/internal/bn_conf.h
/usr/local/include/node/openssl/archs/solaris-x86-gcc/asm_avx2/crypto/include/internal/dso_conf.h
/usr/local/include/node/openssl/archs/solaris-x86-gcc/asm_avx2/include/openssl/opensslconf.h
/usr/local/include/node/openssl/archs/solaris-x86-gcc/asm_avx2/include/progs.h
/usr/local/include/node/openssl/archs/solaris-x86-gcc/no-asm/crypto/buildinf.h
/usr/local/include/node/openssl/archs/solaris-x86-gcc/no-asm/crypto/include/internal/bn_conf.h
/usr/local/include/node/openssl/archs/solaris-x86-gcc/no-asm/crypto/include/internal/dso_conf.h
/usr/local/include/node/openssl/archs/solaris-x86-gcc/no-asm/include/openssl/opensslconf.h
/usr/local/include/node/openssl/archs/solaris-x86-gcc/no-asm/include/progs.h
/usr/local/include/node/openssl/archs/solaris64-x86_64-gcc/asm/crypto/buildinf.h
/usr/local/include/node/openssl/archs/solaris64-x86_64-gcc/asm/crypto/include/internal/bn_conf.h
/usr/local/include/node/openssl/archs/solaris64-x86_64-gcc/asm/crypto/include/internal/dso_conf.h
/usr/local/include/node/openssl/archs/solaris64-x86_64-gcc/asm/include/openssl/opensslconf.h
/usr/local/include/node/openssl/archs/solaris64-x86_64-gcc/asm/include/progs.h
/usr/local/include/node/openssl/archs/solaris64-x86_64-gcc/asm_avx2/crypto/buildinf.h
/usr/local/include/node/openssl/archs/solaris64-x86_64-gcc/asm_avx2/crypto/include/internal/bn_conf.h
/usr/local/include/node/openssl/archs/solaris64-x86_64-gcc/asm_avx2/crypto/include/internal/dso_conf.h
/usr/local/include/node/openssl/archs/solaris64-x86_64-gcc/asm_avx2/include/openssl/opensslconf.h
/usr/local/include/node/openssl/archs/solaris64-x86_64-gcc/asm_avx2/include/progs.h
/usr/local/include/node/openssl/archs/solaris64-x86_64-gcc/no-asm/crypto/buildinf.h
/usr/local/include/node/openssl/archs/solaris64-x86_64-gcc/no-asm/crypto/include/internal/bn_conf.h
/usr/local/include/node/openssl/archs/solaris64-x86_64-gcc/no-asm/crypto/include/internal/dso_conf.h
/usr/local/include/node/openssl/archs/solaris64-x86_64-gcc/no-asm/include/openssl/opensslconf.h
/usr/local/include/node/openssl/archs/solaris64-x86_64-gcc/no-asm/include/progs.h
/usr/local/include/node/openssl/asn1.h
/usr/local/include/node/openssl/asn1_mac.h
/usr/local/include/node/openssl/asn1err.h
/usr/local/include/node/openssl/asn1t.h
/usr/local/include/node/openssl/async.h
/usr/local/include/node/openssl/asyncerr.h
/usr/local/include/node/openssl/bio.h
/usr/local/include/node/openssl/bioerr.h
/usr/local/include/node/openssl/blowfish.h
/usr/local/include/node/openssl/bn.h
/usr/local/include/node/openssl/bn_conf.h
/usr/local/include/node/openssl/bn_conf_asm.h
/usr/local/include/node/openssl/bn_conf_no-asm.h
/usr/local/include/node/openssl/bnerr.h
/usr/local/include/node/openssl/buffer.h
/usr/local/include/node/openssl/buffererr.h
/usr/local/include/node/openssl/camellia.h
/usr/local/include/node/openssl/cast.h
/usr/local/include/node/openssl/cmac.h
/usr/local/include/node/openssl/cms.h
/usr/local/include/node/openssl/cmserr.h
/usr/local/include/node/openssl/comp.h
/usr/local/include/node/openssl/comperr.h
/usr/local/include/node/openssl/conf.h
/usr/local/include/node/openssl/conf_api.h
/usr/local/include/node/openssl/conferr.h
/usr/local/include/node/openssl/crypto.h
/usr/local/include/node/openssl/cryptoerr.h
/usr/local/include/node/openssl/ct.h
/usr/local/include/node/openssl/cterr.h
/usr/local/include/node/openssl/des.h
/usr/local/include/node/openssl/dh.h
/usr/local/include/node/openssl/dherr.h
/usr/local/include/node/openssl/dsa.h
/usr/local/include/node/openssl/dsaerr.h
/usr/local/include/node/openssl/dso_conf.h
/usr/local/include/node/openssl/dso_conf_asm.h
/usr/local/include/node/openssl/dso_conf_no-asm.h
/usr/local/include/node/openssl/dtls1.h
/usr/local/include/node/openssl/e_os2.h
/usr/local/include/node/openssl/ebcdic.h
/usr/local/include/node/openssl/ec.h
/usr/local/include/node/openssl/ecdh.h
/usr/local/include/node/openssl/ecdsa.h
/usr/local/include/node/openssl/ecerr.h
/usr/local/include/node/openssl/engine.h
/usr/local/include/node/openssl/engineerr.h
/usr/local/include/node/openssl/err.h
/usr/local/include/node/openssl/evp.h
/usr/local/include/node/openssl/evperr.h
/usr/local/include/node/openssl/hmac.h
/usr/local/include/node/openssl/idea.h
/usr/local/include/node/openssl/kdf.h
/usr/local/include/node/openssl/kdferr.h
/usr/local/include/node/openssl/lhash.h
/usr/local/include/node/openssl/md2.h
/usr/local/include/node/openssl/md4.h
/usr/local/include/node/openssl/md5.h
/usr/local/include/node/openssl/mdc2.h
/usr/local/include/node/openssl/modes.h
/usr/local/include/node/openssl/obj_mac.h
/usr/local/include/node/openssl/objects.h
/usr/local/include/node/openssl/objectserr.h
/usr/local/include/node/openssl/ocsp.h
/usr/local/include/node/openssl/ocsperr.h
/usr/local/include/node/openssl/opensslconf.h
/usr/local/include/node/openssl/opensslconf_asm.h
/usr/local/include/node/openssl/opensslconf_no-asm.h
/usr/local/include/node/openssl/opensslv.h
/usr/local/include/node/openssl/ossl_typ.h
/usr/local/include/node/openssl/pem.h
/usr/local/include/node/openssl/pem2.h
/usr/local/include/node/openssl/pemerr.h
/usr/local/include/node/openssl/pkcs12.h
/usr/local/include/node/openssl/pkcs12err.h
/usr/local/include/node/openssl/pkcs7.h
/usr/local/include/node/openssl/pkcs7err.h
/usr/local/include/node/openssl/rand.h
/usr/local/include/node/openssl/rand_drbg.h
/usr/local/include/node/openssl/randerr.h
/usr/local/include/node/openssl/rc2.h
/usr/local/include/node/openssl/rc4.h
/usr/local/include/node/openssl/rc5.h
/usr/local/include/node/openssl/ripemd.h
/usr/local/include/node/openssl/rsa.h
/usr/local/include/node/openssl/rsaerr.h
/usr/local/include/node/openssl/safestack.h
/usr/local/include/node/openssl/seed.h
/usr/local/include/node/openssl/sha.h
/usr/local/include/node/openssl/srp.h
/usr/local/include/node/openssl/srtp.h
/usr/local/include/node/openssl/ssl.h
/usr/local/include/node/openssl/ssl2.h
/usr/local/include/node/openssl/ssl3.h
/usr/local/include/node/openssl/sslerr.h
/usr/local/include/node/openssl/stack.h
/usr/local/include/node/openssl/store.h
/usr/local/include/node/openssl/storeerr.h
/usr/local/include/node/openssl/symhacks.h
/usr/local/include/node/openssl/tls1.h
/usr/local/include/node/openssl/ts.h
/usr/local/include/node/openssl/tserr.h
/usr/local/include/node/openssl/txt_db.h
/usr/local/include/node/openssl/ui.h
/usr/local/include/node/openssl/uierr.h
/usr/local/include/node/openssl/whrlpool.h
/usr/local/include/node/openssl/x509.h
/usr/local/include/node/openssl/x509_vfy.h
/usr/local/include/node/openssl/x509err.h
/usr/local/include/node/openssl/x509v3.h
/usr/local/include/node/openssl/x509v3err.h
/usr/local/include/node/uv/aix.h
/usr/local/include/node/uv/android-ifaddrs.h
/usr/local/include/node/uv/bsd.h
/usr/local/include/node/uv/darwin.h
/usr/local/include/node/uv/errno.h
/usr/local/include/node/uv/linux.h
/usr/local/include/node/uv/os390.h
/usr/local/include/node/uv/posix.h
/usr/local/include/node/uv/stdint-msvc2008.h
/usr/local/include/node/uv/sunos.h
/usr/local/include/node/uv/threadpool.h
/usr/local/include/node/uv/tree.h
/usr/local/include/node/uv/unix.h
/usr/local/include/node/uv/version.h
/usr/local/include/node/uv/win.h
/usr/local/include/node/uv.h
/usr/local/include/node/v8-internal.h
/usr/local/include/node/v8-platform.h
/usr/local/include/node/v8-profiler.h
/usr/local/include/node/v8-testing.h
/usr/local/include/node/v8-util.h
/usr/local/include/node/v8-value-serializer-version.h
/usr/local/include/node/v8-version-string.h
/usr/local/include/node/v8-version.h
/usr/local/include/node/v8-wasm-trap-handler-posix.h
/usr/local/include/node/v8-wasm-trap-handler-win.h
/usr/local/include/node/v8.h
/usr/local/include/node/v8config.h
/usr/local/include/node/zconf.h
/usr/local/include/node/zlib.h
/usr/local/share/doc/node/gdbinit
/usr/local/share/doc/node/lldb_commands.py
/usr/local/share/man/man1/node.1
/usr/local/share/systemtap/tapset/node.stp
/usr/local/lib/dtrace/node.d
==> Caveats
Bash completion has been installed to:
  /usr/local/etc/bash_completion.d
==> Summary
🍺  /usr/local/Cellar/node/13.4.0: 4,663 files, 59MB
~$ npm -v
6.13.4
~$ 
```

