# react-native-daylight-saving-date

Sample project to reproduce the issue: [Parsing 'daylight saving date' returns wrong date and time on Android.](https://github.com/facebook/react-native/issues/23657)

This issue has been reporte to [`jsc-android`](https://github.com/react-native-community/jsc-android-buildscripts/issues/88) repository too.

## How to reproduce 

On a emulator or real device: Setup the Android timezone to `'GMT-03:00 Brasilia Standart Time' (or America/Sao_Paulo) (-02:00 when in daylight saving date)`.

<img src="https://raw.githubusercontent.com/douglasjunior/react-native-daylight-saving-date/master/screenshots/timezone-config.png" width="300" />

Clone this repo and run:

```
git clone https://github.com/douglasjunior/react-native-daylight-saving-date.git
cd react-native-daylight-saving-date
yarn install (or npm install)
react-native run-android
```

The [App.js](https://github.com/douglasjunior/react-native-daylight-saving-date/blob/master/App.js) should displays a `alert` popup like this:

<img src="https://raw.githubusercontent.com/douglasjunior/react-native-daylight-saving-date/master/screenshots/alert-wrong-date.png" width="300" />

## Note

The branch `master` uses default React Native `0.58.5` JavaScriptCore, while `jsc` branch uses the [jsc-android](https://github.com/react-native-community/jsc-android-buildscripts) `236355.1.1`.

## Enviroment

```
  React Native Environment Info:
    System:
      OS: macOS High Sierra 10.13.6
      CPU: (4) x64 Intel(R) Core(TM) i5-4278U CPU @ 2.60GHz
      Memory: 187.17 MB / 8.00 GB
      Shell: 3.0.0 - /usr/local/bin/fish
    Binaries:
      Node: 8.14.0 - /usr/local/bin/node
      Yarn: 1.13.0 - /usr/local/bin/yarn
      npm: 6.5.0 - /usr/local/bin/npm
      Watchman: 4.9.0 - /usr/local/bin/watchman
    SDKs:
      iOS SDK:
        Platforms: iOS 11.4, macOS 10.13, tvOS 11.4, watchOS 4.3
      Android SDK:
        API Levels: 16, 17, 18, 19, 21, 22, 23, 24, 25, 26, 27, 28
        Build Tools: 23.0.1, 23.0.3, 24.0.3, 25.0.0, 25.0.1, 25.0.2, 25.0.3, 26.0.1, 26.0.2, 26.0.3, 27.0.3, 28.0.0, 28.0.0, 28.0.1, 28.0.2, 28.0.3
        System Images: android-16 | Google APIs Intel x86 Atom, android-17 | Google APIs Intel x86 Atom, android-19 | Google APIs Intel x86 Atom, android-21 | Google APIs Intel x86 Atom, android-24 | Google Play Intel x86 Atom, android-28 | Google Play Intel x86 Atom
    IDEs:
      Android Studio: 3.2 AI-181.5540.7.32.5014246
      Xcode: 9.4.1/9F2000 - /usr/bin/xcodebuild
    npmPackages:
      react: 16.6.3 => 16.6.3 
      react-native: 0.58.5 => 0.58.5 
    npmGlobalPackages:
      react-native-cli: 2.0.1
```
