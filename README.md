
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

Android:
 Make sure install JAVA jdk
  brew cask install android-sdk
  sdkmanager "emulator"
  sdkmanager "platform-tools"
  sdkmanager "system-images;android-26;google_apis;x86_64"
  avdmanager create avd -n NAME -k "system-images;android-26;google_apis;x86_64" # the one that you use above

  add to .bashrc. use bash or szh, not fist

  export ANDROID_HOME="/usr/local/share/android-sdk"
  export PATH=$PATH:$ANDROID_HOME/emulator
  export PATH=$PATH:$ANDROID_HOME/tools
  export PATH=$PATH:$ANDROID_HOME/tools/bin
  export PATH=$PATH:$ANDROID_HOME/platform-tools
  export ANDROID_SDK_ROOT=$ANDROID_HOME
  alias emu="$ANDROID_HOME/tools/emulator"