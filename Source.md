0xbench project is hosted at http://gitorious.org/0xbench/. Follow below steps, it shows how to set up the building environment, how to download 0xbench source code and how to build-from-scratch.

# Download Source Code #
Use git to clone the source tree from Gitorious:
```
git clone git://gitorious.org/0xbench/0xbench.git
```

# Building APK (SDK) #
An APK image contains all the built-in Java-based benchmarks and a interface to the native C-based benchmarks, but not the C binaries itself.

## Using Ant ##
  1. Download and install Android SDK. Instruction can be found on [developer.android.com](http://developer.android.com/sdk/index.html).
  1. Generate local settings file (local.properties) by invoking the command:
```
android update project --path /path/to/0xbench/
```
  1. In the project directory (0xbench/), use one of the following commands to build APK depend on your needs:
```
ant debug     // generate a debug APK, you need to setup debug keystore in advance
ant release   // generate a debug APK, you need to setup release keystore in advance
ant install   // install directly to connected device or emulator
```
  1. The produced APK file can be found under `/path/to/0xbench/bin/`. You can now deploy it to you devices using adb:
```
cd /path/to/0xbench
adb install bin/Benchmark-*.apk
```

## Using Eclipse ##
  1. Download and install Android SDK and Eclipse IDE. Instruction can be found on [developer.android.com](http://developer.android.com/sdk/index.html).
  1. In Eclipse, click `File` -> `New` -> `Android Project`.
  1. In the new project dialog, select  `Create project from existing source` , select the path to 0xbench.
  1. Click Finish to create project in Eclipse.

# Building and Deploying Standalone Binaries (NDK) #

  1. Download and install both Android SDK and Android NDK. Instruction can be found on [developer.android.com/sdk](http://developer.android.com/sdk/index.html) and [developer.android.com/sdk/ndk](http://developer.android.com/sdk/ndk/index.html).
  1. In the project directory (0xbench), build binaries with the command:
```
/path/to/ndk/ndk-build
```
  1. The binaries can be found under `/path/to/0xbench/libs/armeabi/bench_*`. Use root permission to mount `/system` with rw permission, and use adb to deploy:
```
adb push /path/to/0xbench/libs/armeabi/bench_* /system/bin/
```

# Building Everything with Source Tree (0xdroid) #
  1. Download and build the 0xdroid source tree. Instructions can be found in [0xdroid wiki](http://code.google.com/p/0xdroid/wiki/Source).
  1. Setup build environment:
```
cd /path/to/0xdroid/
source build/envsetup.sh
export TOP=`pwd`
```
  1. Build APK and binaries:
```
cd /path/to/0xbench/
mm
```
  1. APK and binaries can be found in:
```
//APK
/path/to/0xdroid/target/product/arch/system/app/ZeroXBenchmark.apk
//Binaries
/path/to/0xdroid/target/product/arch/system/bin/bench_*
```