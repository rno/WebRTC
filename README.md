# WebRTC Binaries for Android
[![Latest version](https://img.shields.io/github/v/release/rno/webrtc)](https://github.com/rno/WebRTC/releases)
[![Release Date](https://img.shields.io/github/release-date/rno/webrtc)](https://github.com/rno/WebRTC/releases)
[![Total Downloads](https://img.shields.io/github/downloads/rno/webrtc/total)](https://github.com/rno/WebRTC/releases)
[![Maven Central](https://img.shields.io/maven-central/v/com.dafruits/webrtc)](https://github.com/rno/WebRTC/releases)


This repository contains unofficial distribution of WebRTC framework binaries for Android. This is heavily inspired by the work for providing [WebRTC binaries for iOS and MacOS](https://github.com/stasel/WebRTC).

Since version M80, Google has [deprecated](https://groups.google.com/g/discuss-webrtc/c/Ozvbd0p7Q1Y/m/M4WN2cRKCwAJ?pli=1) their mobile binary libraries distributions (Was officially using the JCenter). To get the most up to date WebRTC library, you can compile it on your own, or you can use precompiled binaries from here or other sources.

## 📦 Releases
The binary releases correspond with official Chromium releases and branches as specified in the [Chromium dashboard](https://chromiumdash.appspot.com/branches).

## 💡 Things to know
All binaries in this repository are compiled from the official WebRTC [source code](https://webrtc.googlesource.com/src/) without any modifications to the source code or to the output binaries.

## 📢 Requirements
* minSdkVersion = 21

## 📀 Binaries included

* arm64-v8a
* armeabi-v7a
* x86
* x86_64

## 🚚 Installation

### Maven

The latest release is available on [Maven Central](https://search.maven.org/artifact/com.dafruits/webrtc/120.0.0/aar)

#### Gradle Groovy DSL

```groovy
implementation 'com.dafruits:webrtc:120.0.0'
```

#### Gradle Kotlin DSL

```kotlin
implementation("com.dafruits:webrtc:120.0.0")
```

### Manual
1. Download the AAR from the [releases](https://github.com/rno/WebRTC/releases) section.
2. Copy the AAR file into a `libs` folder inside your app folder.
3. Include the following line in the `dependencies` section of your `build.gradle.kts` file

```kotlin
implementation(files("libs/libwebrtc-120.0.0.aar"))
```

### Proguard

```
-keep class org.webrtc.** { *; }
```

## 🛠 Compile your own WebRTC AAR
If you wish to compile your own WebRTC AAR, please refer to the following official guide:
https://webrtc.googlesource.com/src/+/refs/heads/main/docs/native-code/android/

## 📃 License
* WebRTC License: https://webrtc.org/support/license