
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

Run Android
Make sure install JAVA jdk

``` 
  brew cask install android-sdk
  sdkmanager "emulator"
  sdkmanager "platform-tools"
  sdkmanager "system-images;android-26;google_apis;x86_64"
  avdmanager create avd -n NAME -k "system-images;android-26;google_apis;x86_64" # the one that you use above
```

  add to .bashrc. use bash or szh, not fish

```
  export ANDROID_HOME="/usr/local/share/android-sdk"
  export PATH=$PATH:$ANDROID_HOME/emulator
  export PATH=$PATH:$ANDROID_HOME/tools
  export PATH=$PATH:$ANDROID_HOME/tools/bin
  export PATH=$PATH:$ANDROID_HOME/platform-tools
  export ANDROID_SDK_ROOT=$ANDROID_HOME
  alias emu="$ANDROID_HOME/tools/emulator"
```

Add permission for application
AndroidManifest.xml

```
<uses-permission android:name="android.permission.INTERNET" />
<uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" />
<uses-permission android:name="android.permission.CAMERA" />
<uses-permission android:name="android.permission.RECORD_AUDIO" />

```

If got unexpect close application, try:

gradle.properties
```
android.enableDexingArtifactTransform.desugaring=false
