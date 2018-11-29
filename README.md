# react-native-notes
Notes About errors, fixes, tips tricks and things to remember for React Native mobile apps Development

# "Unable to load script from assets 'index.android.bundle'..."
just edit "package.json" file, and add this code
```
"android-linux": "react-native bundle --platform android --dev false --entry-file index.js --bundle-output android/app/src/main/assets/index.android.bundle --assets-dest android/app/src/main/res && react-native run-android"
```
![GitHub Logo](/images/logo.png)
Format: ![Alt Text](url)
