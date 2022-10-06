
npx react-native init pitelsdk3
yarn add pitel-sdk-webrtc
yarn add pitel-react-native-webrtc

Ios: 
  add to ios/<...>/Info.plist; before </dict>

  <key>NSMicrophoneUsageDescription</key>
  <string>Need microphone access for voip call</string>

  npx react-native run-ios

  If get error  ERROR Invariant Violation: `new NativeEventEmitter()` requires a non-null argument.

  cd ios/
  pod install
  cd .. 
  npx react-native run-ios


