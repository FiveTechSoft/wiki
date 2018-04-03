For iOS (iPhone/iPad). Next post is for simulator:

[url]https://bitbucket.org/fivetech/harbour-xharbour-builds/downloads/harbour_ios_20160401.zip[/url]

[b]To build it:[/b]
git clone https://github.com/harbour/core.git [color=#FF0000]harbour_ios[/color]

ios.sh      (remember to do chmod +x ios.sh. To execute it ./ios.sh)

#!/bin/bash

export IPHONEOS_DEPLOYMENT_TARGET="8.0"
export QTPATH=/Users/$USER/Qt/5.6/ios

export IOS_PLAT=/Applications/Xcode.app/Contents/Developer/Platforms/[color=#FF0000]iPhoneOS.platform[/color]
export IOS_DEFAULT=/Applications/Xcode.app/Contents/Developer/Toolchains/XcodeDefault.xctoolchain
export PATH="/Users/$USER/[color=#FF0000]harbour_ios[/color]/bin/production:$IOS_PLAT/Developer/usr/bin:$IOS_PLAT/Developer/usr/local/bin:$IOS_PLAT/usr/bin:$IOS_PLAT/usr/local/bin:/Applications/Xcode.app/Contents/Developer/Tools:$IOS_DEFAULT/usr/bin:$IOS_DEFAULT/usr/libexec:/usr/bin:/bin:/usr/sbin:/sbin:/usr/local/bin"

export SDK_INCLUDE=$IOS_PLAT/Developer/SDKs/[color=#FF0000]iPhoneOS.sdk[/color]/usr/include
export SDK_LIB=$IOS_PLAT/Developer/SDKs/iPhoneOS.sdk/usr/lib
export SDK_LIB_SYSTEM=$IOS_PLAT/Developer/SDKs/iPhoneOS.sdk/usr/lib/system

export HB_BUILD_NAME=-iphone
export __ios__=yes

export HB_HOST_BIN=/Users/$USER/[color=#FF0000]harbour[/color]/bin/darwin/clang

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

export HB_USER_CFLAGS=[color=#FF0000]-arch\ armv7\ -arch\ arm64\ [/color]-DHB_MAIN_WIN\ -DHB_BUILD_IOS\ -I$SDK_INCLUDE
export HB_USER_DFLAGS=[color=#FF0000]-arch\ armv7\ -arch\ arm64\[/color] -L$SDK_LIB\ -L$SDK_LIB_SYSTEM
export HB_USER_LDFLAGS=[color=#FF0000]-arch\ armv7\ -arch\ arm64\[/color] -L$SDK_LIB\ -L$SDK_LIB_SYSTEM

export HB_STATIC_QT=yes
export HB_QT_MAJOR_VERSION=5
export HB_QTPATH=$QTPATH/bin
export HB_WITH_QT=$QTPATH/include

#export HB_BUILD_3RDEXT=no

export HB_STATIC_OPENSSL=1
export HB_WITH_OPENSSL=/Users/$USER/[color=#FF0000]harbour_ios[/color]/openssl-1.0.1k/include

make