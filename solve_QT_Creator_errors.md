[Android build sdk not defined](https://forum.qt.io/topic/83476/android-build-sdk-not-defined-check-android-settings-qt-5-9-1-qtcreator-4-4-0-with-android-studio/16)

```
I found a strange solution:

closed qtcreator

I edited the *pro.user file of my project.
there are some entries::
<value type="QString" key="BuildTargetSdk"></value>
<value type="QString" key="KeystoreLocation"></value>

3: I changed every occurence of
<value type="QString" key="BuildTargetSdk"></value>
to
<value type="QString" key="BuildTargetSdk">android-26</value>

(26 is my android sdk tools main version)

4: Now I can deploy again to my smartphone.

Strange is: the combobox "Android build Sdk" still is empty... doesn't matter now...
```

QT "Could not determine java version from 10" or 9:

Install Java NDK 8 and gets solved

