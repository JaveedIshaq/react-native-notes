# react-native-notes
Notes About errors, fixes, tips tricks and things to remember for React Native mobile apps Development

# "Unable to load script from assets 'index.android.bundle'..."
just edit "package.json" file, and add this code
```
"android-linux": "react-native bundle --platform android --dev false --entry-file index.js --bundle-output android/app/src/main/assets/index.android.bundle --assets-dest android/app/src/main/res && react-native run-android"
```

# objects are not valid as a react child (found: object with keys {$$typeof, type, key, ref, props, _owner, _store}). if you meant to render a collection of children, use an array instead.
```
"dependencies": {
"firebase": "^5.5.9",
"react": "16.6.1",
"react-native": "0.57.7",
"react-native-material-kit": "^0.5.1",
"react-native-vector-icons": "^6.1.0"
}, 
```
with above dependencies, I managed to solve this issue by doing following
```
import firebase from '@firebase/app';
```
# Clean the Android Project

```
  cd android
  
  .\gradlew clean
```

