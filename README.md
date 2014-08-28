Google AdMob extension for OpenFL applications. 
Working on Android. 
Not working on iOS, but the original repo had an outdated version.
Forked from https://github.com/mkorman9/admob-openfl

**Instructions**

1. Clone this repo using ```haxelib git admob https://github.com/charcoal/admob-openfl``` command
2. Add this line to your project.xml file ```<haxelib name="admob" /> ```
3. Import AD class ```import admob.AD; ```
4. Setup ads at the beginning of your code 
```AD.init(ADMOB_ID, AD.LEFT, AD.BOTTOM, AD.BANNER_PORTRAIT, ?DEVICE_ID);```
```AD.initInterstitial(ADMOB_ID, ?DEVICE_ID);```
where arguments are following:
  - Ad unit id.
  - Position in x axis. Could be ```AD.LEFT``` or ```AD.RIGHT```
  - Position in y axis. Could be ```AD.TOP``` or ```AD.BOTTOM```
  - Banner size. Could be ```AD.BANNER_PORTRAIT``` or ```AD.BANNER_LANDSCAPE``` (see google's documentation)
  - Device ID. Set a device to show only test Ads. Optional.
5. Show Banner Ad ```AD.show();```
6. Show Interstitial Ad ```AD.showInterstitial();```
7. You can hide the Banner Ad anytime by calling ```AD.hide();```

**Prerequisites on Android**

1. Copy the file ids.xml to the root directory of the project.
2. Replace **Google_App_ID** in ids.xml with the Game Services App ID from the Google Play Developer Console.
3. Add following code to your project.xml:
```<template path="ids.xml" rename="res/values/ids.xml" if="android" />```
