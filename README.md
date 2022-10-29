1) Download flutter. ( https://docs.flutter.dev/get-started/install/macos )
2) navigate to your flutter folder.
3) Run command
```bash
# Add flutter to PATH
export PATH="$PATH:`pwd`/bin"
```
4) Download command line tools (on https://developer.android.com/studio/command-line/sdkmanager)
5) navigate to your command-line tools folder.
6) Run command
```bash
# Add command-line tools to PATH
export PATH="$PATH:`pwd`/bin"
```
7) Run commands
```bash
# Define ANDROID_HOME, if not defined already
export ANDROID_HOME="~/Library/Android/sdk"

# Create the folder if missing
mkdir -p $ANDROID_HOME

# Let the tool know that it should use that SDK location. 
sdkmanager --list --sdk_root=$ANDROID_HOME

# Install SDK
sdkmanager --install "cmdline-tools;latest" --sdk_root=~/Library/Android/sdk
```
8) Run `flutter doctor`
You should see something like
```
Doctor summary (to see all details, run flutter doctor -v):
[✓] Flutter (Channel stable, 3.3.6, on macOS 13.0 22A380 darwin-arm, locale en-NL)
[✓] Android toolchain - develop for Android devices (Android SDK version 33.0.0)
[✓] Xcode - develop for iOS and macOS (Xcode 14.0.1)
[✓] Chrome - develop for the web
[✓] Android Studio (version 2021.3)
[✓] Android Studio (version 2021.3)
[✓] IntelliJ IDEA Ultimate Edition (version 2022.1.3)
[✓] IntelliJ IDEA Ultimate Edition (version EAP IU-222.3345.16)
[✓] VS Code (version 1.72.2)
[✓] Connected device (2 available)
[✓] HTTP Host Availability

• No issues found!
```
