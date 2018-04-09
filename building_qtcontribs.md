**export QTPATH=/Users/$USER/Qt/5.8/ios**

**export HB_QTPATH=$QTPATH/bin**

**export HB_WITH_QT=$QTPATH/include**

to check them:

**echo "$HB_QTPATH"**

**export HB_USER_CFLAGS="-std=c++11"**

**/Users/$USER/harbour/bin/darwin/clang/hbmk2 hbqscintilla.hbp**

from harbour/contribs/qtcontribs/hbqt/qscintilla

clang -c -I../qtcore -I/Users/$USER/harbour/include -I$HB_QTPATH/include -std=c++11 -arch arm64 -I/Applications/Xcode.app/Contents/Developer/Platforms/iPhoneOS.platform/Developer/SDKs/iPhoneOS.sdk/usr/include -Wno-nullability-completeness hbqt_init.cpp

clang -c -I../qtcore -I/Users/$USER/harbour/include -I$HB_QTPATH/include/** -std=c++14 -arch arm64 -Iz:\Users\anto\QScintilla_gpl-2.10.3\Qt4Qt5 -Wno-nullability-completeness -I/Applications/Xcode.app/Contents/Developer/Platforms/iPhoneOS.platform/Developer/SDKs/iPhoneOS.sdk/usr/include/** hbqt_hbqsciscintilla.cpp

clang -c -I$HB_QTPATH/include -std=c++11 -arch arm64 -isysroot/Applications/Xcode.app/Contents/Developer/Platforms/iPhoneOS.platform/Developer/SDKs/iPhoneOS.sdk -I/Users\$USER/QScintilla_gpl-2.10.3/Qt4Qt5/** -I/Users/$USER/harbour/include -I../qtcore -Wno-nullability-completeness hbqt_hbqsciscintilla.cpp

clang -c -O3 -std=c++14 -Wno-nullability-completeness -I/Users/anto/Qt/5.10.1/ios/include/QtCore -I/Users/anto/Qt/5.10.1/ios/include/QtWidgets -I/Users/anto/Qt/5.10.1/ios/include/QtGui -I/Users/anto/Qt/5.10.1/ios/include/QtPrintSupport -DHBMK_HAS_QT -W -Wall -I/Users/anto/harbour/include -I../../../.. -I../../../../qscintilla -I../../../../qtcore -I../../../../qtgui -I/Users/anto/Qt/5.10.1/ios/include '../../../../qscintilla/hbqt_init.cpp' '../../../../qscintilla/hbqt_hbqsciscintilla.cpp' '../../../../.hbmk/darwin/clang/hbqscintilla/moc_hbqt_hbqsciscintilla.cpp' ../../../../.hbmk/darwin/clang/hbqscintilla/HBQsciScintilla.cpp ../../../../.hbmk/darwin/clang/hbqscintilla/QsciAbstractAPIs.cpp ../../../../.hbmk/darwin/clang/hbqscintilla/QsciAPIs.cpp ../../../../.hbmk/darwin/clang/hbqscintilla/QsciCommand.cpp ../../../../.hbmk/darwin/clang/hbqscintilla/QsciCommandSet.cpp ../../../../.hbmk/darwin/clang/hbqscintilla/QsciDocument.cpp ../../../../.hbmk/darwin/clang/hbqscintilla/QsciLexer.cpp ../../../../.hbmk/darwin/clang/hbqscintilla/QsciScintilla.cpp ../../../../.hbmk/darwin/clang/hbqscintilla/QsciStyle.cpp ../../../../.hbmk/darwin/clang/hbqscintilla/QsciStyledText.cpp


namespace std
{
   template <class T> T swap( T t1, T t2 ){}
   template <class T> struct add_const{ T t; };
   template <class T> T move( T t ) { return t; }
   template <class T> struct decay;
   template <class T> T forward( T t );
   template <class T> struct is_enum;
   template <class T> struct is_integral;
   template <bool B, class T = void> struct enable_if;
}
