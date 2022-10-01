# Setup Flutter Development Environment

References:

- https://docs.flutter.dev/get-started/install/macos

## Setup

Install xcode command line tools

``` shell
sudo xcode-select --install
sudo xcode-select --switch /Applications/Xcode.app/Contents/Developer
```

Enable Rosetta 2

``` shell
sudo softwareupdate --install-rosetta --agree-to-license
```

Download Flutter SDK
The latest SDK is `flutter_macos_arm64_3.3.3-stable.zip` for now.
https://storage.googleapis.com/flutter_infra_release/releases/stable/macos/flutter_macos_arm64_3.3.3-stable.zip


``` shell
curl -O https://storage.googleapis.com/flutter_infra_release/releases/stable/macos/flutter_macos_arm64_3.3.3-stable.zip
```

Unzip and update PATH

``` shell
unzip flutter_macos_arm64_3.3.3-stable.zip
export PATH="$(pwd)/flutter/bin:$PATH"
```

I've used `direnv` to configure tha `PATH` in the directory.

``` shell
echo 'export PATH="$(pwd)/flutter/bin:$PATH"' > .direnv
```


Check installation

``` shell
flutter doctor
```

Example output:

``` text

```


Install

Android Studio

Create a new project.
Open 'Tools' > 'SDK Manager' > 'SDK Tools' tab
Select 'Android SDK Command-line Tools (latest)' then press 'Applly' button

% flutter doctor --android-licenses

XCode
execute 
% sudo xcode-select --switch /Applications/Xcode.app/Contents/Developer
Password:
% sudo xcodebuild -runFirstLaunch


Cocoapods

rbenv install 2.7.6
rbenv local 2.7.6
bundle init
bundle add cocoapods
