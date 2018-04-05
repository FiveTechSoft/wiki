**Important:** Avoid the next steps and simply [download it already built from here](https://github.com/FiveTechSoft/fivetouch/blob/master/Harbour%20for%20Android/Harbour_for_Android_with_QT_and_Scintilla_libs.zip)

***

In order to build Harbour for Android, please follow these steps:

   * [Download Harbour source code from here](https://github.com/harbour/core) you may use git:

   >git clone https://github.com/harbour/core.git harbour

   * [Download qtcontribs from here](https://sourceforge.net/projects/qtcontribs) you may use svn:

   >```
   >svn checkout https://svn.code.sf.net/p/qtcontribs/code/trunk qtcontribs
   >```

   >or simply download the source code from [here](https://sourceforge.net/p/qtcontribs/code/HEAD/tree/) clicking on "Download Snapshot"

   >Create a c:\harbour\contrib\qtcontribs folder and copy there the qtcontribs sources and
   >add this line to c:\harbour\contrib\hbplist.txt:

   > qtcontribs/qtcontribs.hbp

   * [Download QT open source from here](https://www.qt.io/download) and install it

   * [Download Android NDK from here](https://developer.android.com/ndk/downloads/index.html) select the Windows 64-bit
and unzip it at c:\android\ndk 

**1.** Create Harbour for MinGW. We use the MinGW distributed with QT:

**Important:** If harbour has been created previously with another compiler
do a win-make clean

gomingw.bat
```
set path=c:\Qt\Tools\mingw530_32

win-make
```

**2.** Create Harbour for Android:

(Use the next goand.bat and avoid this step) Run this batch file: http://forums.fivetechsupport.com/viewtopic.php?p=170850#p170850

It will create this batch file that finally creates Harbour for Android:

goand.bat
```
#!msdos

@echo off

set HB_PLATFORM=android
set HB_COMPILER=gccarm
set HB_CCPREFIX=C:\android\ndk\toolchains\arm-linux-androideabi-4.9\prebuilt\windows-x86_64\bin\arm-linux-androideabi-
set HB_INSTALL_PREFIX=C:\harbour

set HB_USER_CFLAGS=--sysroot=C:\android\ndk\platforms\android-14\arch-arm -IC:\android\ndk\sources\cxx-stl\gnu-libstdc++\4.9\include -IC:\android\ndk\sources\cxx-stl\gnu-libstdc++\4.9\libs\armeabi-v7a\include -IC:\android\ndk\platforms\android-14\arch-arm\usr\include -Ic:\android\ndk\sysroot\usr\include
set HB_USER_DFLAGS=--sysroot=C:\android\ndk\platforms\android-14\arch-arm
set HB_USER_LDFLAGS=--sysroot=C:\android\ndk\platforms\android-14\arch-arm -lm
win-make
```

**3.** To speed up the creation of qtcontribs, create it after creating Harbour and use this batch file
running it from c:\harbour\contrib\qtcontribs:

go.bat
```
@echo off

set HB_PLATFORM=android
set HB_COMPILER=gccarm
set HB_CCPREFIX=C:\android\ndk\toolchains\arm-linux-androideabi-4.9\prebuilt\windows-x86_64\bin\arm-linux-androideabi-
set HB_INSTALL_PREFIX=C:\harbour

set QT_PATH=C:\Qt\5.4\android_armv7
set HB_WITH_QT=%QT_PATH%\include
set HB_QTPATH=%QT_PATH%\bin

set HB_USER_CFLAGS=--sysroot=C:\android\ndk\platforms\android-14\arch-arm -IC:\android\ndk\sources\cxx-stl\gnu-libstdc++\4.9\include -IC:\android\ndk\sources\cxx-stl\gnu-libstdc++\4.9\libs\armeabi-v7a\include -IC:\android\ndk\platforms\android-14\arch-arm\usr\include -Ic:\android\ndk\sysroot\usr\include
set HB_USER_DFLAGS=--sysroot=C:\android\ndk\platforms\android-14\arch-arm
set HB_USER_LDFLAGS=--sysroot=C:\android\ndk\platforms\android-14\arch-arm -lm

c:\harbour\bin\hbmk2 qtcontribs.hbp
```

***
[![](https://bitbucket.org/fivetech/screenshots/downloads/harbour.jpg)](https://github.com/harbour/core "The Harbour Project")