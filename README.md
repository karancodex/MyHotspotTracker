React Native Hotspot Device Tracker App

This is a React Native app designed to track devices connected to your mobile hotspot. It uses a native module to read the ARP table from Android and display connected devices, and provides a UI to manage hotspot detection and user prompts.

🔧 Technologies Used

React Native (TypeScript)

Java (Native Module for Android)

Metro Bundler

Android Gradle Build System

ChatGPT (for Kotlin logic reference and explanation)

🚀 Features

Automatically fetch devices connected to your phone's Wi-Fi hotspot (using Android's ARP table)

Displays IP, MAC address, and device name

Shows a dialog when the hotspot is turned off and asks user to manually turn it on (due to OS-level limitations)

Simple UI for checking devices and prompting actions

🧭 How to Use This App

✅ Please make sure you have completed the React Native Environment Setup before continuing.

Step 1: Install dependencies and start Metro

npm install
npm start

Step 2: Run the app on Android

npm run android

📲 App Usage Instructions

Open the app

If your hotspot is already ON, the app will automatically fetch and display all connected Wi-Fi devices.

If your hotspot is OFF, a dialog will appear:

It will ask you to manually start your hotspot

Due to platform restrictions, React Native cannot automatically enable hotspot

After starting hotspot manually, press "Refresh" to fetch the connected devices.

If data is not fetched after refresh, close and reopen the app to fetch properly.

📝 Notes

This app only works on Android due to platform limitations (no ARP table on iOS).

Permissions required:

android.permission.ACCESS_WIFI_STATE

android.permission.INTERNET

android.permission.ACCESS_NETWORK_STATE

🔔 Important

Note: If the data is not fetched after pressing the refresh button, please close and reopen the app. The data will then be displayed correctly.

Learning Update: I used ChatGPT during this development process because I am not yet familiar with Kotlin. However, since Kotlin seems to be an important skill in your company, I have started learning it actively.

📦 Building APK (Android)

To generate a signed APK:

cd android
./gradlew assembleRelease

APK file will be located at:

android/app/build/outputs/apk/release/app-release.apk

For debug builds:

./gradlew assembleDebug

🤝 Contribution

If you'd like to contribute or extend this app (e.g., integrate Firebase, use Kotlin Jetpack APIs, or add auto hotspot toggle via root access), feel free to fork and raise PRs!

📚 Learn More

React Native Docs

Kotlin for Android

Android Networking & ARP

Made with ❤️ using React Native