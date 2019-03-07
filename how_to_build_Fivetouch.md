**1**. Download QT Creator from here:

https://www.qt.io/download

**2**. Open fivetouch.pro from QT Creator

**3** Download Java JDK from here:

https://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html

**4** Download Android NDK from here:

https://developer.android.com/ndk/downloads

**5** QT Creator settings

Android SDK location: (install Android Studio so the right one gets installed!)
/Users/anto/Library/Android/sdk

Android NDK location:

/Users/anto/android-ndk-r18b

![](https://github.com/FiveTechSoft/fivetouch/blob/master/images/QT_Creator_Settings.png)

**6**. Build it 

If you get errors that can't identify, go to:
/Users/username/fivetouch/build-fivetouch-Android_for_armeabi_v7a_Clang_Qt_5_12_1_for_Android_ARMv7-Release
and call make. You will see what the QT Creator Makefile reports.