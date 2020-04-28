# AndroidReverseEngineering
all about android reverse engineering

## Getting APK from mobile
```
>> adb shell pm list packages
>> abd pull /data/app/apkfile.apk
```
## Apktools decoding/build
```
apktool d apkfile.apk -o apkfolder
```
```
apktool b apkfolder
```

## Generating keystore file
```
keytool -genkey -v -keystore my-release-key.keystore -alias alias_name -keyalg RSA -keysize 2048 -validity 10000
```
## Sign the apk file
```
jarsigner -verbose -sigalg SHA1withRSA -digestalg SHA1 -keystore my-release-key.keystore app-debug.apk alias_name
```

## Tools
* [Apktools](https://ibotpeaches.github.io/Apktool/)
* dex2jar
* Android Studio
   * sdk 
   * emulator
* keytools
* jarsigner

## Links 
[Unofficial Google Play API](https://github.com/egirault/googleplay-api)
[Chrome Extension](https://chrome.google.com/webstore/detail/apk-downloader/fgljidimohbcmjdabiecfeikkmpbjegm?hl=en)
[Smali Plugin installation](https://crosp.net/blog/software-development/mobile/android/android-reverse-engineering-debugging-smali-using-smalidea/)





