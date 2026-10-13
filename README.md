<div align="center">

# ⏰ Alarm Animation App

### Mobile Application Development · Practical 6

A native Android application built with **Kotlin, XML layouts, and Android animation APIs**. The project demonstrates an animated splash screen, frame-by-frame image animations, and a Material-styled alarm interface.

<br>

![Platform](https://img.shields.io/badge/Platform-Android-3DDC84?style=for-the-badge&logo=android&logoColor=white)
![Language](https://img.shields.io/badge/Language-Kotlin-7F52FF?style=for-the-badge&logo=kotlin&logoColor=white)
![UI](https://img.shields.io/badge/UI-XML%20%7C%20ConstraintLayout-4285F4?style=for-the-badge&logo=android)
![Build](https://img.shields.io/badge/Build-Gradle-02303A?style=for-the-badge&logo=gradle&logoColor=white)

**[View Repository](https://github.com/jayshilpatel29/24012021038_pr6_mad)**

</div>

---

## 📖 About the Project

**Alarm Animation App** is an Android Mobile Application Development practical project. It focuses on using Android's animation resources to create a moving institute logo on the splash screen and animated graphics on the main screen.

The main screen presents an alarm-themed interface with an animated alarm image, a pulsing heart graphic, short instructional text, and **Create Alarm** and **Cancel Alarm** buttons in the layout.

> **Implementation note:** In the current source code, the Create Alarm and Cancel Alarm buttons are part of the UI, but their click handlers and actual alarm-scheduling/cancellation logic have not been implemented yet. The project currently demonstrates the interface and animations rather than a fully functioning alarm scheduler.

## ✨ Features in the Current Code

- **Animated splash screen** — displays a sequence of UVPCE logo images using an Android `AnimationDrawable`.
- **Tween animation** — applies translate, rotate, and scale transformations to the splash-screen logo.
- **Automatic screen transition** — opens `MainActivity` when the splash animation ends.
- **Alarm image animation** — cycles through ten alarm images using a frame animation list.
- **Pulsing heart animation** — cycles through heart images to create a pulse effect.
- **ConstraintLayout interface** — arranges the main screen content responsively using constraints.
- **Material card design** — places the alarm content inside a `MaterialCardView` with rounded corners and elevation.
- **Edge-to-edge support** — handles system-bar insets in both activities.

## 🧰 Tech Stack

| Technology | How it is used |
|---|---|
| Kotlin | Activity code and animation control |
| Android SDK | Native Android app framework |
| XML layouts | Screen layouts and UI components |
| `AnimationDrawable` | Frame-by-frame drawable animations |
| Android View Animation | Translate, rotate, and scale effects |
| ConstraintLayout | Positioning and arranging UI elements |
| Material Components | `MaterialCardView` and Material styling |
| AndroidX AppCompat / Core / Activity | Activity compatibility and Android UI support |
| Gradle Kotlin DSL | Build and dependency configuration |

## 🖼️ App Flow

```text
Launch Application
       │
       ▼
  SplashActivity
       │
       ├── UVPCE logo frame animation
       ├── Translate / rotate / scale animation
       │
       ▼
   MainActivity
       │
       ├── Animated alarm images
       ├── Animated heart graphic
       └── Create Alarm / Cancel Alarm buttons
           (UI only in the current implementation)
```

## 📁 Project Structure

```text
24012021038_pr6_mad/
├── app/
│   ├── build.gradle.kts
│   └── src/
│       ├── main/
│       │   ├── java/com/jayshil/a24012021038_pr6_mad/
│       │   │   ├── SplashActivity.kt
│       │   │   └── MainActivity.kt
│       │   ├── res/
│       │   │   ├── anim/
│       │   │   │   └── twinanimation.xml
│       │   │   ├── drawable/
│       │   │   │   ├── alarm_animation_list.xml
│       │   │   │   ├── heart_animation_list.xml
│       │   │   │   ├── uvpce_animation_list.xml
│       │   │   │   └── animation image assets
│       │   │   ├── layout/
│       │   │   │   ├── activity_splash.xml
│       │   │   │   └── activity_main.xml
│       │   │   └── AndroidManifest.xml
│       │   ├── androidTest/
│       │   └── test/
│       └── ...
├── gradle/
├── build.gradle.kts
├── settings.gradle.kts
├── gradle.properties
├── gradlew
└── gradlew.bat
```

## ⚙️ Requirements

- [Android Studio](https://developer.android.com/studio)
- A compatible Android SDK (the project is configured with **compile SDK 36, minor API level 1**)
- Android SDK Platform 26 or later for the configured minimum SDK
- An Android emulator or a physical Android device
- Internet access during the initial Gradle sync if dependencies need to be downloaded

**Project configuration:**

- Application ID: `com.jayshil.a24012021038_pr6_mad`
- Minimum SDK: `26`
- Target SDK: `36`
- Version: `1.0` (`versionCode` 1)
- Source/target compatibility: Java 11

## 🚀 Run the Project

### Option 1 — Android Studio

1. Clone or download this repository.
2. Open Android Studio and select **Open**.
3. Select the project folder `24012021038_pr6_mad`.
4. Allow Gradle to sync and install any required SDK components.
5. Start an emulator or connect an Android phone with USB debugging enabled.
6. Select the app run configuration and click **Run ▶**.

### Option 2 — Command line

On Windows, from the project root:

```bat
gradlew.bat assembleDebug
```

On macOS or Linux:

```bash
./gradlew assembleDebug
```

If the build succeeds, the debug APK is normally generated at:

```text
app/build/outputs/apk/debug/app-debug.apk
```

### Clone the repository

```bash
git clone https://github.com/jayshilpatel29/24012021038_pr6_mad.git
```

Then open the downloaded project folder in Android Studio.

## 🧠 Concepts Demonstrated

This practical provides hands-on experience with:

- Android activity lifecycle basics (`onCreate` and window-focus changes)
- Navigating from a splash activity to a main activity using an `Intent`
- Defining frame animations with XML `<animation-list>` resources
- Starting and stopping `AnimationDrawable` animations
- Loading tween animations from XML with `AnimationUtils`
- Building an interface with `ConstraintLayout`, `TextView`, `ImageView`, `Button`, and `MaterialCardView`
- Handling system-bar insets for edge-to-edge layouts
- Organizing Android resources and build dependencies

## 🔧 Possible Next Steps

- Connect the **Create Alarm** button to Android's alarm APIs, such as `AlarmManager` and a suitable `PendingIntent`.
- Implement the **Cancel Alarm** button so it cancels the matching scheduled alarm.
- Add a time picker and display the selected alarm time.
- Add runtime notification permission handling where required by the Android version and notification design.
- Add screenshots or a short screen recording of the app running.
- Test the app on multiple screen sizes and Android versions.

These are suggested improvements, not features already implemented in the current code.

## 👨‍💻 Developer

**Jayshil Patel**  
**Enrollment No.:** `24012021038`  
**Course:** Mobile Application Development (MAD)  
**Practical:** 6  
**GitHub:** [@jayshilpatel29](https://github.com/jayshilpatel29)

## 📄 License

This repository does not currently specify an open-source license. Please contact the repository owner before reusing or redistributing the project beyond permitted academic use.

---

<div align="center">

**Built for learning Android development, one practical at a time.** 💚

</div>
