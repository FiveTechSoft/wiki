For iOS (iPhone/iPad):

[Download here Harbour for iOS](https://bitbucket.org/fivetech/harbour-xharbour-builds/downloads/harbour_ios_20160401.zip)

**or build it:**

1. git clone https://github.com/harbour/core.git **harbour_ios**

2. go to harbour_ios/contrib and create a folder qtcontribs:

>mkdir qtcontribs

3. Download qtcontribs source code there:

>git clone https://github.com/FiveTechSoft/qtcontribs qtcontribs

4. go to qtcontribs folder and edit qtcontribs.hbp:

>nano qtcontribs.hbp

>comment out this line:

>#debug/hwgdebug.hbp

>and add this new line:

>hbqt/qtcore/qscintilla.hbp

5. Finally go to contribs folder, edit hbplist.txt and this line at the top:

>qtcontribs/qtcontribs.hbp



ios.sh      (remember to do chmod +x ios.sh. To execute it ./ios.sh)
```
#!/bin/bash

export IPHONEOS_DEPLOYMENT_TARGET="8.0"
export QTPATH=/Users/$USER/Qt/5.8/ios

export IOS_PLAT=/Applications/Xcode.app/Contents/Developer/Platforms/iPhoneOS.platform
export IOS_DEFAULT=/Applications/Xcode.app/Contents/Developer/Toolchains/XcodeDefault.xctoolchain
export PATH="/Users/$USER/harbour_ios/bin/production:$IOS_PLAT/Developer/usr/bin:$IOS_PLAT/Developer/usr/local/bin:$IOS_PLAT/usr/bin:$IOS_PLAT/usr/local/bin:/Applications/Xcode.app/Contents/Developer/Tools:$IOS_DEFAULT/usr/bin:$IOS_DEFAULT/usr/libexec:/usr/bin:/bin:/usr/sbin:/sbin:/usr/local/bin"

export SDK_INCLUDE=$IOS_PLAT/Developer/SDKs/iPhoneOS.sdk/usr/include
export SDK_LIB=$IOS_PLAT/Developer/SDKs/iPhoneOS.sdk/usr/lib
export SDK_LIB_SYSTEM=$IOS_PLAT/Developer/SDKs/iPhoneOS.sdk/usr/lib/system

export HB_BUILD_NAME=-iphone
export __ios__=yes

export HB_HOST_BIN=/Users/$USER/harbour/bin/darwin/clang

export HB_WITH_PCRE=local
export HB_WITH_ZLIB=local
export HB_WITH_BZIP2=local
export HB_WITH_JPEG=local
export HB_WITH_PNG=local
export HB_WITH_TIFF=local
export HB_WITH_LIBHARU=local
export HB_WITH_SQLITE3=local

export HB_BUILD_DYN=no
export HB_BUILD_PARTS=lib

export HB_USER_CFLAGS=-arch\ armv7\ -arch\ arm64\ -DHB_MAIN_WIN\ -DHB_BUILD_IOS\ -I$SDK_INCLUDE
export HB_USER_DFLAGS=-arch\ armv7\ -arch\ arm64\ -L$SDK_LIB\ -L$SDK_LIB_SYSTEM
export HB_USER_LDFLAGS=-arch\ armv7\ -arch\ arm64\ -L$SDK_LIB\ -L$SDK_LIB_SYSTEM

export HB_STATIC_QT=yes
export HB_QT_MAJOR_VERSION=5
export HB_QTPATH=$QTPATH/bin
export HB_WITH_QT=$QTPATH/include

#export HB_BUILD_3RDEXT=no

export HB_STATIC_OPENSSL=1
export HB_WITH_OPENSSL=/Users/$USER/harbour_ios/openssl-1.0.1k/include

make
```
***
This one is working nicely for Qt 5.8:
```
export IPHONEOS_DEPLOYMENT_TARGET="8.0"
export QTPATH=/Users/$USER/Qt/5.8/ios

export IOS_PLAT=/Applications/Xcode.app/Contents/Developer/Platforms/iPhoneOS.platform
export IOS_DEFAULT=/Applications/Xcode.app/Contents/Developer/Toolchains/XcodeDefault.xctoolchain
export PATH="/Users/$USER/harbour_ios/bin/production:$IOS_PLAT/Developer/usr/bin:$IOS_PLAT/Developer/usr/local/bin:$IOS_PLAT/usr/bin:$IOS_PLAT/usr/local/bin:/Applications/Xcode.app/Contents/Developer/Tools:$IOS_DEFAULT/usr/bin:$IOS_DEFAULT/usr/libexec:/usr/bin:/bin:/usr/sbin:/sbin:/usr/local/bin"

export SDK_INCLUDE=$IOS_PLAT/Developer/SDKs/iPhoneOS.sdk/usr/include
export SDK_INCLUDEXX=$SDK_INCLUDE\c++
export SDK_LIB=$IOS_PLAT/Developer/SDKs/iPhoneOS.sdk/usr/lib
export SDK_LIB_SYSTEM=$IOS_PLAT/Developer/SDKs/iPhoneOS.sdk/usr/lib/system

export HB_BUILD_NAME=-iphone
export __ios__=yes

export HB_HOST_BIN=/Users/$USER/harbour/bin/darwin/clang

export HB_WITH_PCRE=local
export HB_WITH_ZLIB=local
export HB_WITH_BZIP2=local
export HB_WITH_JPEG=local
export HB_WITH_PNG=local
export HB_WITH_TIFF=local
export HB_WITH_LIBHARU=local
export HB_WITH_SQLITE3=local

export HB_BUILD_DYN=no
export HB_BUILD_PARTS=lib

export HB_USER_CFLAGS=-std=c++11\ -I$SDK_INCLUDE\ -I$SDK_INCLUDEXX\ -I/Users/$USER/QScintilla_gpl-2.10.3/Qt4Qt5\ -Wno-nullability-completeness\ -arch\ armv7\ -arch\ arm64\ -DHB_MAIN_WIN\ -DHB_BUILD_IOS\
export HB_USER_DFLAGS=-arch\ armv7\ -arch\ arm64\ -L$SDK_LIB\ -L$SDK_LIB_SYSTEM
export HB_USER_LDFLAGS=-arch\ armv7\ -arch\ arm64\ -L$SDK_LIB\ -L$SDK_LIB_SYSTEM

export HB_STATIC_QT=yes
export HB_QT_MAJOR_VERSION=5
export HB_QTPATH=$QTPATH/bin
export HB_WITH_QT=$QTPATH/include

#export HB_BUILD_3RDEXT=no

export HB_STATIC_OPENSSL=1
export HB_WITH_OPENSSL=/Users/$USER/harbour_ios/openssl-1.0.1k/include

make 
```