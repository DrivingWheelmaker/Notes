# ReactNative

> 写在前面：
>
> 本文是我做移动端开发的笔记。虽然跟我们的网站框架没有关系，不过可以从中借鉴到React框架的知识。作为和Vue并驾齐驱（其实，在全世界范围内看，React才是主流，毕竟Vue只是在国内还可以）的前端框架，我们可以从React与Vue的对比中增长一些见识。

# Title

References 

>[Chinese Tutorial](http://reactnative.cn/docs/tutorial/)
>
>[English Toturial](https://reactnative.dev/docs/tutorial)



## 1. Getting Started: Environment

1. `brew install node` take a `long` time.

2. `brew install watchman` quickly finished.
3. `sudo gem install cocoapods` quick.
4. Open command line tool in Xcode: `Xcode | Preferences | Locations`.
5. `npx react-native init AwesomeProject` in VScode terminal.

```command line
~/Projects/PetAPP$ npx react-native init AwesomeProject
                                                          
               ######                ######                        
            ##          ###    ###          ##            
            ##             ####             ##                 
            ##         ###      ###         ##            
             ##  ########################  ##             
          ######    ###            ###    ######          
      ###     ##    ##              ##    ##     ###      
  ##           ####      ########      ####           ##  
 ##             ###     ##########     ###             ## 
  ##           ####      ########      ####           ##  
      ###     ##    ##              ##    ##     ###      
          ######    ###            ###    ######          
             ##  ########################  ##             
            ##         ###      ###         ##            
            ##             ####             ##                   
            ##          ###    ###          ##                       
               ######                ######               
                                                          

                  Welcome to React Native!                
                 Learn once, write anywhere               

? Directory "AwesomeProject" already exists, do you want to replace it? Yes
✔ Downloading template
✔ Copying template
✔ Processing template
✔ Installing CocoaPods dependencies (this may take a few minutes)

  Run instructions for iOS:
    • cd "/Users/yanghaowen/Projects/PetAPP/AwesomeProject" && npx react-native run-ios
    - or -
    • Open AwesomeProject/ios/AwesomeProject.xcworkspace in Xcode or run "xed -b ios"
    • Hit the Run button

  Run instructions for Android:
    • Have an Android emulator running (quickest way to get started), or a device connected.
    • cd "/Users/yanghaowen/Projects/PetAPP/AwesomeProject" && npx react-native run-android

~/Projects/PetAPP$
```

6.`cd AwesomeProject` and ` yarn ios`.

```
~/Projects/PetAPP/AwesomeProject$ yarn ios
yarn run v1.22.0
$ react-native run-ios
info Found Xcode workspace "AwesomeProject.xcworkspace"
info Launching iPhone 11 (iOS 13.3)
info Building (using "xcodebuild -workspace AwesomeProject.xcworkspace -configuration Debug -scheme AwesomeProject -destination id=EE8E36AB-7396-413F-B84D-5544AC449590")
....................
info Installing "/Users/yanghaowen/Library/Developer/Xcode/DerivedData/AwesomeProject-bnhnexafuyagtlfoktfmxjyodfty/Build/Products/Debug-iphonesimulator/AwesomeProject.app"
info Launching "org.reactjs.native.example.AwesomeProject"
success Successfully launched the app on the simulator
✨  Done in 82.22s.
```

<img src="/Users/yanghaowen/Projects/Notes/References/Images/node-launchpacker-command_when_first_init_react_native_application.jpg" alt="node_launchpacker_command when first init react native application" style="zoom: 50%;" />

Simulator will pop out:

<img src="/Users/yanghaowen/Projects/Notes/References/Images/awsome_app_on_vm.jpg" alt="Screen Shot 2020-02-29 at 10.40.55 AM" style="zoom:33%;" />

Then we've finished prepareing the environment of react native.



## 2. HelloWorld

### Do:

1. Overwrite `App.js`:

   ```
   import React, { Component } from 'react';
   import { Text, View } from 'react-native';
   
   export default class HelloWorldApp extends Component {
     render() {
       return (
           <View style={{ flex: 1, justifyContent: "center", alignItems: "center" }}>
             <Text>Hello, world!</Text>
           </View>
       );
     }
   }
   ```

2. `cd AwesomeProject` and ` yarn ios`.
3. and see the simulator:

<img src="/Users/yanghaowen/Projects/Notes/References/Images/helloworld.jpg" alt="Screen Shot 2020-02-29 at 10.53.00 AM" style="zoom: 33%;" />

### Explain:

ES2015 (also ES6): 



## Problem Solving

### error Could not find the following native modules: RNVectorIcons. Did you forget to run "pod install" ?

How to run `pod install?` ?

First, anywhere, run `sudo gem install cocoapods`. (If cocapods already exist, no need, no harm)

`cd ios` and `ls` to see whether have an `PROJECT_NAME.xcodeproj`. If so, good.

Use `pod init`. if already have `pod`, no harm, just throw `[!] Existing Podfile found in directory`.

Main operation: `pod install`.

```
$ pod install
Detected React Native module pods for RNCMaskedView, RNGestureHandler, RNReanimated, RNScreens, RNVectorIcons, and react-native-safe-area-context
Analyzing dependencies
Downloading dependencies
Installing RNVectorIcons (6.6.0)
Generating Pods project
Integrating client project
Pod installation complete! There are 34 dependencies from the Podfile and 32 total pods installed.
```

like so. Install dependencies you don't have. Then will run good.

### Unrecognized font family 'Ionicons'

`yarn react-native link`

```
yarn run v1.22.0
$ /Users/yanghaowen/Projects/ZMAPP/zmapp/node_modules/.bin/react-native link
info Linking assets to ios project
info Linking assets to android project
success Assets have been successfully linked to your project
✨  Done in 1.49s.
```

Can solve this, TEMPORARILY. 

when you run-ios next time, will face issue:

```
ERROR: Failed to build iOS project. We ran "xcodebuild" command but it exited with error code 65. 
...
```

And now `yarn react-native unlink react-native-vector-icons` can fix it.

But the link between react-native and react-native-vector-icons is GONE again...

This is related to auto link issues in RN 6.0, and RVcector-icons is out of date and didn't fix it.

Solution: **DO NOT USE IT.** sigh...



### Package has been Ignored because it contains Invalid Configuration React Native Error Fix

This react native warning will finally leads to build error while trying to run your application. So, how to fix this particular error? All you need is to run *npm install* command on your terminal from your project folder. After that try running your project again using either *react-native run-android* or *react-native run-ios*command.



