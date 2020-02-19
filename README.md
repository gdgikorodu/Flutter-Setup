<h1>Getting Started Flutter</h1>
<p>Explaining how to setup flutter for Windows and Mac users using VS Code or Android Studio</p>
<h2>Some links for more in-depth learning</h2>
<h3><a id="user-content-setting-startedsetup" class="anchor" href="https://github.com/gdgikorodu/Flutter-Setup#setting-startedsetup" aria-hidden="true"></a>Setting started/setup</h3>
<ul>
<li><a href="https://flutter.dev/docs/get-started/install/windows" rel="nofollow">Getting Started With Flutter - Windows</a></li>
<li><a href="https://flutter.dev/docs/get-started/install/macos" rel="nofollow">Getting Started With Flutter - Mac</a></li>
<li><a href="https://flutter.dev/docs/get-started/install/linux" rel="nofollow">Getting Started With Flutter - Linux</a></li>
</ul>
<h3><a id="user-content-purely-text-based-resources" class="anchor" href="https://github.com/gdgikorodu/Flutter-Setup#purely-text-based-resources" aria-hidden="true"></a>Purely text-based resources</h3>
<ul>
<li><a href="https://flutter.dev/docs" rel="nofollow">Documentation</a>&nbsp;Tutorials, samples, guidance on mobile development, and a full API reference.</li>
<li><a href="https://flutter.dev/docs/get-started/codelab" rel="nofollow">Lab: Write your first Flutter app</a>&nbsp;Flutter codelabs.</li>
<li><a href="https://flutter.dev/docs/cookbook" rel="nofollow">Cookbook: Useful Flutter samples</a>&nbsp;Flutter cookbook.</li>
</ul>
<h1><a id="user-content-setting-up-vs-code-purely" class="anchor" href="https://github.com/gdgikorodu/Flutter-Setup#setting-up-vs-code-purely" aria-hidden="true"></a>Setting up VS Code purely</h1>
<h3>Windows</h3>
<ul>
<li>Java Development Kit -&nbsp;<a href="https://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html" rel="nofollow">Install JDK here</a>. Take note of the installation directory as we would have to add to path.&nbsp;<a href="https://javatutorial.net/set-java-home-windows-10" rel="nofollow">Adding JDK to path</a></li>
<li>Download flutter SDK latest version from the following Url:&nbsp;<a href="https://flutter.io/docs/get-started/install/windows" rel="nofollow">https://flutter.io/docs/get-started/install/windows</a>&nbsp;extract it and copy the folder with the name &ldquo;flutter&rdquo; to C:\ folder, so the full path will be C:\flutter</li>
<li>Download the Android command line tools -&nbsp;<a href="https://developer.android.com/studio/index.html#downloads" rel="nofollow">Android Command Line Tools</a>, extract after downloading. Create the folder "Android" in C:\Users\USER\AppData\Local and the folder Sdk in C:\Users\USER\AppData\Local\Android and copy the tools folder here.</li>
<li>Set the environment variables - we need to define some environment variable which let the above tools know how to contact each other, form command prompt run these commands, one by one.
<ul>
<li><em>setx ANDROID_HOME "C:\Users\USER\AppData\Local\Android"</em></li>
<li><em>ANDROID_SDK_ROOT "C:\Users\USER\AppData\Local\Android\Sdk"</em></li>
<li><em>path "%path%;"C:\Users\USER\AppData\Local\Android\Sdk;C:\Users\USER\AppData\Local\Android\Sdk\bin;C:\flutter\bin"</em></li>
</ul>
</li>
<li>Download Android Sdk - As you may already know Flutter needs Android SDK to work , so we need to download system images, platform tools, build tools, platforms, and emulator, by running the following commands:
<ul>
<li><em>sdkmanager "system-images;android-29;google_apis;x86_64"</em></li>
<li><em>sdkmanager "platforms;android-29"</em></li>
<li><em>sdkamanger "platform-tools"</em></li>
<li><em>sdkmanager "patcher;v4"</em></li>
<li><em>sdkmanager "emulator"</em></li>
<li><em>sdkmanager "build-tools;29.0.2"</em></li>
</ul>
</li>
<li>Accept all licenses (press y then enter for every license)
<ul>
<li><em>sdkmanager --licenses</em></li>
</ul>
</li>
<li>Configure flutter to know the directory of the android sdk
<ul>
<li><em>flutter config --android-sdk C:\Users\USER\AppData\Local\Android\</em></li>
</ul>
</li>
<li>Create the emulator (use any of the below to create the emulator)
<ul>
<li>create an emulator with the name pixel:<em> avdmanager -s create avd -n pixel -k "system-images;android-29;google_apis;x86_64"</em></li>
<li>create an emulator with the name nexus: <em>avdmanager -s create avd -n nexus -k "system-images;android-29;default;x86_64"</em></li>
<li>create an emulator using existing devices features: <em>avdmanager -s create avd -n pixel -k "system-images;android-29;google_apis;x86_64" -d 19</em></li>
<li>to get list of existing devices: <em>avdmanager list</em></li>
</ul>
</li>
<li>Launch emulator
<ul>
<li><em>flutter emulator --launch emulator_name</em></li>
</ul>
</li>
<li>Now to the moment of truth
<ul>
<li>Run <em>flutter doctor</em>. This command should give all green and ok. Please ignore the Android Studio complain as this lesson is all about ignoring it.</li>
</ul>
</li>
</ul>
<h3>Mac</h3>
<ul>
<li>Watch this space</li>
</ul>