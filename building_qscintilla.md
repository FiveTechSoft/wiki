export IPHONEOS_DEPLOYMENT_TARGET="8.0"
export QTPATH=/Users/$USER/Qt/5.8/ios

export IOS_PLAT=/Applications/Xcode.app/Contents/Developer/Platforms/iPhoneOS.platform
export IOS_DEFAULT=/Applications/Xcode.app/Contents/Developer/Toolchains/XcodeDefault.xctoolchain
#export PATH="$IOS_PLAT/Developer/usr/bin:$IOS_PLAT/Developer/usr/local/bin:$IOS_PLAT/usr/bin:$IOS_PLAT/usr/local/bin:/Applications/Xcode.app/Contents/Developer/Tools:$IOS_DEFAULT/usr/bin:$IOS_DEFAULT/usr/libexec:/usr/bin:/bin:/usr/sbin:/sbin:/usr/local/bin"

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

export HB_USER_CFLAGS="-I/Users/$USER/QScintilla_gpl-2.10.3/Qt4Qt5 -std=c++11 -DHB_MAIN_WIN\ -DHB_BUILD_IOS\ -I$SDK_INCLUDE"
export HB_USER_DFLAGS=-L$SDK_LIB
export HB_USER_LDFLAGS=-L$SDK_LIB

export HB_STATIC_QT=yes
export HB_QT_MAJOR_VERSION=5
export HB_QTPATH=$QTPATH/bin
export HB_WITH_QT=$QTPATH/include

export HB_STATIC_OPENSSL=1
export HB_WITH_OPENSSL=/Users/$USER/harbour_ios/openssl-1.0.1k/include

#export QT_PLUGIN_PATH=/usr/local/opt/qt5/plugins/

#export HB_WITH_QT=/usr/local/opt/qt5/include/

#export HB_QT_MAJOR_VER=5

/Users/$USER/harbour/bin/darwin/clang/hbmk2 hbqscintilla.hbp

