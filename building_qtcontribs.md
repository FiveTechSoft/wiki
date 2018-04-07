from harbour/contribs/qtcontribs/hbqt/qscintilla

clang -c -I../qtcore -I/Users/$USER/harbour/include -I$HB_QTPATH/include -std=c++11 -arch arm64 -I/Applications/Xcode.app/Contents/Developer/Platforms/iPhoneOS.platform/Developer/SDKs/iPhoneOS.sdk/usr/include hbqt_init.cpp


clang -c -I../qtcore -I/Users/$USER/harbour/include -I$HB_QTPATH/include -std=c++14 -arch arm64 -I/Applications/Xcode.app/Contents/Developer/Platforms/iPhoneOS.platform/Developer/SDKs/iPhoneOS.sdk/usr/include/c++\4.2.1\tr1 -Iz:\Users\anto\QScintilla_gpl-2.10.3\Qt4Qt5 -I$HB_QTPATH/include/QtCore -Wno-nullability-completeness hbqt_hbqsciscintilla.cpp
