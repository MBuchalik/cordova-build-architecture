# cordova-build-architecture
This plugin allows you to build your application for arm (or x86) only.
# Why?
Plugins like cordova-plugin-crosswalk-webview (https://github.com/crosswalk-project/cordova-plugin-crosswalk-webview) create two or more .apk files with one build. On Phonegap Build, you can only download one file which leads to problems if you want to get access to the other .apks.

Also, the Crosswalk plugin sometimes creates a combined arm/x86 file on Phonegap Build even if you set the preference *xwalkMultipleApk* to *true*.

Maybe you simply need to build for one architecture because of other reasons? This plugin might help you :-)

# Usage
Include this plugin in your config.xml:
``` xml
<plugin name="cordova-build-architecture" spec="https://github.com/MBuchalik/cordova-build-architecture.git#v1.0.3" source="git" />
```

By default, it will try to produce arm builds only. If you want to target x86, add the following preference:
``` xml
<preference name="buildArchitecture" value="x86" />
```

**Please note that this plugin is experimental.**
