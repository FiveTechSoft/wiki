Go to QT creator, Projects, "Buils steps" and add a "custom process step" and fill the info as in the attached picture.

Using the go up arrow, place that step as the first one.

QT build settings:

Command: c:\harbour\bin\harbour

Arguments: c:\fivetouch\fivetouch.prg /n -oc:\fivetouch\fivetouch.c -Ic:\harbour\include

Working directory: %{buildDir}
![](https://github.com/FiveTechSoft/fivetouch/blob/master/images/Compile_PRGs_from_QT_Creator.jpg)