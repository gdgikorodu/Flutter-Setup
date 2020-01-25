Getting Started Flutter
===================================

Explaining how to setup flutter for Windows and Mac users using VS Code or Android Studio

## Some links for more in depth learning
### Setting started/setup
* [Getting Started With Flutter - Windows](https://flutter.dev/docs/get-started/install/windows)
* [Getting Started With Flutter - Mac](https://flutter.dev/docs/get-started/install/macos)
* [Getting Started With Flutter - Linux](https://flutter.dev/docs/get-started/install/linux)

### Purely text based resources
* [Documentation](https://flutter.dev/docs) Tutorials, samples, guidance on mobile development, and a full API reference.
* [Lab: Write your first Flutter app](https://flutter.dev/docs/get-started/codelab) Flutter codelabs.
* [Cookbook: Useful Flutter samples](https://flutter.dev/docs/cookbook) Flutter cookbook.


Setting up VS Code purely
============================
### Windows
* Java Developmenty Kit - [Install JDK here](https://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html). Take note of the installation directory as we would have to add to path. [Adding JDK to path](https://javatutorial.net/set-java-home-windows-10)
* Download flutter sdk latest version from following url: https://flutter.io/docs/get-started/install/windows extract it, and copy the folder with the name “flutter” to C:\ folder, so the full path will be C:\flutter
* Download the Android command line tools - [Android Command Line Tools](https://developer.android.com/studio/index.html#downloads), extract after downloading. Create the folder "Android" in C:\Users\USER\AppData\Local and the foler Sdk in C:\Users\USER\AppData\Local\Android and copy the tools folder here.
* Set the environment variables - We need to define some environment variable which let the above tools know how to contact each other, form command prompt run these commands, one by one.
  - setx ANDROID_HOME "C:\Users\USER\AppData\Local\Android"
  - ANDROID_SDK_ROOT "C:\Users\USER\AppData\Local\Android\Sdk"
  - path "%path%;"C:\C:\Users\USER\AppData\Local\Android\Sdk;C:\C:\Users\USER\AppData\Local\Android\Sdk\bin;C:\flutter\bin"
* Download Android Sdk - As you may already know Flutter needs Android SDK to work , so we need to download system images, platform tools, build tools, platforms, and emulator, by running the following commands:
  - sdkmanager "system-images;android-29;google_apis;x86_64"
  - sdkmanager "platforms;android-29"
  - sdkamanger "platform-tools"
  - sdkmanager "patcher;v4"
  - sdkmanager "emulator"
  - sdkmanager "build-tools;29.0.2"
* Accept all licenses (press y then enter for every license)
  - sdkmanager — -licenses
* Configure flutter to know the directory of the android sdk
  - flutter config — -android-sdk C:\Users\USER\AppData\Local\Android\
* Create the emulator (use any of the below to create the emulator)
  - create an emulator with the name pixel: avdmanager -s create avd -n pixel -k "system-images;android-29;google_apis;x86_64"
  - create an emulator with the name nexus: avdmanager -s create avd -n nexus -k "system-images;android-29;default;x86_64"
  - create an emulator using existing devices features: avdmanager -s create avd -n pixel -k "system-images;android-29;google_apis;x86_64" -d 19
  - to get list of existing devices: avdmanager list
* Launch emulator
  - flutter emulator --launch emulator_name
* Now to the moment of truth
  - Run flutter doctor. This command should give all green and ok. Please ignore the Android Studio complain as this lesson is all about ignoring it.

### Mac