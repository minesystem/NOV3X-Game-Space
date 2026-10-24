NØV3X GAME SPACE — ANDROID STUDIO PROJECT

WHAT THIS IS
A small native Android shell that opens the existing NØV3X Game Space HTML prototype inside an Android WebView. The HTML, CSS, and JavaScript app is bundled locally, so the interface does not need a web server.

REQUIREMENTS
- A computer (Windows, macOS, or Linux)
- Android Studio (stable version)
- Android SDK Platform 35 installed through Android Studio SDK Manager
- JDK 17 (Android Studio's bundled JDK is usually suitable)
- Android phone with USB debugging enabled OR an Android emulator

OPEN THE PROJECT
1. Extract NOV3XGameSpaceAndroid.zip to a folder.
2. Open Android Studio.
3. Choose Open and select the extracted NOV3XGameSpaceAndroid folder (the one containing settings.gradle.kts).
4. Wait for Gradle sync to finish. If asked to install SDK Platform 35 or Build Tools, accept.
5. If Android Studio asks about Gradle JDK, choose the bundled JDK 17.
6. To test, connect your Android phone with USB debugging enabled, or start an emulator.
7. Press Run ▶ and select the device.

BUILD AN INSTALLABLE DEBUG APK
1. In Android Studio, select Build > Build Bundle(s) / APK(s) > Build APK(s).
2. Wait for the build to complete.
3. Click "locate" in the notification, or find:
   app/build/outputs/apk/debug/app-debug.apk
4. Transfer app-debug.apk to your Android phone and open it to install.
5. If Android blocks the install, allow "Install unknown apps" for the app you used to open the APK, then install it. Only install APKs you built or trust.

BUILD A RELEASE APK
1. Select Build > Generate Signed Bundle / APK.
2. Choose APK, then create/select a keystore and keep its password safe.
3. Choose the release build variant and finish the wizard.
4. Use the signed APK output shown by Android Studio.

IMPORTANT LIMITATIONS
- This project is a starter shell, not a production-verified release. Build it in Android Studio and test on a real phone.
- It bundles the prototype's current web interface. The Boost button is an in-app mode only; it does not overclock the device or clear Android system RAM.
- A WebView cannot reliably read another game's true FPS, cellular/Wi-Fi signal strength in dBm, or game-server ping. Those need native Android APIs, permissions, and/or supported integrations.
- The Internet permission is included for network checking; most UI functions work offline.
- Do not share a release keystore or its password.
