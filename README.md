# calender-app

S6 CSE KTU 2019 exam calender
..and yes it only works for this specific purpose and the code is crap and specific

![screenshot](https://i.imgur.com/yFSpagF.jpg)


## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Run your tests
```
npm run test
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).

# To build for android

```
npm run cordova-build-android
```

saved to `/src-cordova/platforms/android/app/build/outputs/apk/release/`

## Sign Android app to install

```
java -jar uber-apk-signer-1.0.0.jar --apks app-release-unsigned.apk 
```

Thanks: [Uber apk Signer](https://github.com/patrickfav/uber-apk-signer)