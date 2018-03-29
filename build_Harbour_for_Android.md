build.bat
```
@echo off

set SYSROOT=C:\android\ndk\platforms\android-9\arch-arm

set HB_PLATFORM=android
set HB_COMPILER=gccarm
set HB_CCPREFIX=C:\android\ndk\toolchains\arm-linux-androideabi-4.9\prebuilt\windows-x86_64\bin\arm-linux-androideabi-
set HB_INSTALL_PREFIX=C:\harbour

set HB_USER_CFLAGS=--sysroot=C:\android\ndk\platforms\android-14\arch-arm -IC:\android\ndk\sources\cxx-stl\gnu-libstdc++\4.9\include -IC:\android\ndk\sources\cxx-stl\gnu-libstdc++\4.9\libs\armeabi-v7a\include -IC:\android\ndk\platforms\android-9\arch-arm\usr\include -Ic:\android\ndk\sysroot\usr\include
set HB_USER_DFLAGS=--sysroot=C:\android\ndk\platforms\android-14\arch-arm
set HB_USER_LDFLAGS=--sysroot=C:\android\ndk\platforms\android-14\arch-arm -lm
win-make
```