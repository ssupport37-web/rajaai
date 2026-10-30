# RAJA AI (Android, Kotlin + Jetpack Compose + Material 3)

Gemini-powered JARVIS-style assistant. Roman Urdu / Urdu / English.

## Build with Android Studio (recommended)
1. Open the `RajaAI` folder in Android Studio (Koala or newer). It syncs Gradle automatically.
2. Run on a phone, or Build > Build APK(s). Output: `app/build/outputs/apk/debug/app-debug.apk`.
3. Open the app > Settings > paste your Gemini API key (free from https://aistudio.google.com) > Test Connection.

## Build from the command line (PC / Linux / Mac)
Needs JDK 17 and the Android SDK (platform 34, build-tools 34). Set `ANDROID_HOME`.
```
gradle wrapper --gradle-version 8.7
./gradlew assembleDebug
```

## Termux
Android's official build tools are x86 builds, so a normal Gradle build usually fails inside Termux (aapt2 problem).
Realistic options: build on a PC, or push this folder to GitHub and use a GitHub Actions Android workflow,
then download the APK onto the phone.

## What works
Chat with context, voice in/out (tap the mic), interrupt speech, offline commands
("open YouTube", "open WhatsApp", "settings kholo", "youtube par <song> search karo"), apps list with search,
favourites and recents, coding mode with copy/save, encrypted settings, dark/light theme, clear history.

## Not included yet
Room chat history database (history is in memory), wake word, accessibility tap-control, weather,
notes/reminders, web search API, notifications.
