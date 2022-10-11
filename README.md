
Download

```shell
git clone git@github.com:TEKERS-VN/pitel-react-native-demo2.git
```

Installation dependencies

```shell
npx react-native init pitelsdk3
yarn add pitel-sdk-webrtc
yarn add pitel-react-native-webrtc
```

For Ios - add to Info.plist

```xml
  <key>NSMicrophoneUsageDescription</key>
  <string>Need microphone access for voip call</string>
```

Run IOS

```
  npx react-native run-ios
```

  If get error  ERROR Invariant Violation: `new NativeEventEmitter()` requires a non-null argument.

```shell
  cd ios/
  pod install
  cd .. 
  npx react-native run-ios
```

