**1**. Download QT Creator from here:

https://www.qt.io/download

**2**. Open fivetouch.pro from QT Creator

**3** Download Java JDK from here:

https://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html

**4** Download Android NDK from here:

https://developer.android.com/ndk/downloads

**5** QT Creator settings

**Java JDK location:**

Run this from the terminal:
/usr/libexec/java_home

and you will get:
/Library/Java/JavaVirtualMachines/jdk1.8.0_202.jdk/Contents/Home

**Android SDK location:** (install Android Studio so the right one gets installed!)
/Users/anto/Library/Android/sdk

**Android NDK location:**

/Users/anto/Library/Android/sdk/ndk-bundle

![](https://github.com/FiveTechSoft/screenshots/blob/master/QT_Creator_Settings2.png)

**6**. Build it 

If you get errors that can't identify, go to:
/Users/username/fivetouch/build-fivetouch-Android_for_armeabi_v7a_Clang_Qt_5_12_1_for_Android_ARMv7-Release
and call make. You will see what the QT Creator Makefile reports.