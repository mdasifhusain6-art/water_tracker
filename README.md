<div align="center">

  <img src="assets/images/app_icon.png" alt="Water Tracker Logo" width="128" height="128" style="border-radius: 28px; box-shadow: 0 12px 32px rgba(2, 136, 209, 0.35);" />

  # 💧 Water Tracker

  **Smart, Mindful & Offline-First Daily Hydration Companion**

  [![Flutter](https://img.shields.io/badge/Flutter-3.x-02569B?style=for-the-badge&logo=flutter&logoColor=white)](https://flutter.dev)
  [![Dart](https://img.shields.io/badge/Dart-3.x-0175C2?style=for-the-badge&logo=dart&logoColor=white)](https://dart.dev)
  [![Supabase](https://img.shields.io/badge/Supabase-Backend-3ECF8E?style=for-the-badge&logo=supabase&logoColor=white)](https://supabase.com)
  [![Android](https://img.shields.io/badge/Android-API%2024%2B-3DDC84?style=for-the-badge&logo=android&logoColor=white)](https://developer.android.com)
  [![License](https://img.shields.io/badge/License-Proprietary-blue?style=for-the-badge)](#license)

  <br>

  <p align="center">
    <strong>Designed & Developed with ❤️ by <a href="https://dhtechnology.in" target="_blank">MD ASIF HUSAIN</a></strong>
  </p>

  <p align="center">
    <a href="#-key-features">Key Features</a> •
    <a href="#-tech-stack">Tech Stack</a> •
    <a href="#-architecture">Architecture</a> •
    <a href="#-getting-started">Getting Started</a> •
    <a href="#-legal--compliance">Compliance</a> •
    <a href="#-author">Author</a>
  </p>

  <br>

  <img src="assets/images/app_preview.png" alt="Water Tracker Mobile App Showcase" width="100%" style="border-radius: 18px; box-shadow: 0 16px 48px rgba(0, 0, 0, 0.4);" />

</div>

---

## 📱 App Preview & Visual Identity

<div align="center">
  <table>
    <tr>
      <td align="center" width="30%">
        <img src="assets/images/app_icon.png" width="140" style="border-radius: 32px; box-shadow: 0 10px 28px rgba(2, 136, 209, 0.35);" /><br><br>
        <strong>Official App Icon</strong><br>
        <sub>Adaptive • Full-Bleed Azure</sub>
      </td>
      <td align="center" width="70%">
        <img src="assets/images/app_preview.png" width="100%" style="border-radius: 14px;" /><br><br>
        <strong>Fluid Dark Mode Interface</strong><br>
        <sub>Live Hydration Tracker, Quick-Add & Analytics</sub>
      </td>
    </tr>
  </table>
</div>

---

## 📖 Overview

**Water Tracker** is a state-of-the-art mobile application engineered to help individuals build, sustain, and celebrate healthy daily hydration habits. Built with an **offline-first philosophy**, it couples instantaneous local interactions powered by **Hive** with cloud resilience and cross-device sync powered by **Supabase**.

Featuring a custom fluid-simulation UI, animated hydration progress visualizations, intelligent notification intervals calibrated to your sleep cycle, and comprehensive intake analytics, **Water Tracker** transforms daily hydration into an effortless, mindful habit.

---

## ✨ Key Features

- ⚡ **Instant Water Logging:** Quick-add presets (250ml, 500ml, 750ml, custom amounts) with haptic feedback and instant single-tap undo capability.
- 🧘 **Dynamic Human Hydration Visualization:** Real-time animated body hydration level indicator with smooth wave animations and celebratory milestones.
- 📊 **Insightful Analytics & Trends:** Interactive daily, weekly, and monthly bar/line charts built with `fl_chart` to monitor streaks, averages, and goals.
- ⏰ **Smart Sleep-Aware Reminders:** Background notifications scheduled via `flutter_local_notifications` that respect your sleep schedule and waking hours.
- 📶 **100% Offline-First Architecture:** Log water entries without active internet. Unsynced changes are queued in encrypted local Hive storage and auto-synchronized when back online.
- 🎨 **Modern Adaptive UI:** Custom glassmorphic styling, refined dark and light modes, and responsive layouts tailored for both smartphones and tablets.
- 🌍 **Internationalization (i18n):** Native localized interface supporting 9 global languages:
  * English (`en`), Hindi (`hi`), Spanish (`es`), French (`fr`), German (`de`), Arabic (`ar`), Portuguese (`pt`), Chinese (`zh`), Japanese (`ja`).
- 🛡️ **Play Store 2026 Compliant:** Fully equipped legal center including Privacy Policy, Terms of Service, and automated Account/Data Deletion workflows.

---

## 🛠️ Tech Stack

| Layer | Technology |
| :--- | :--- |
| **Framework** | [Flutter](https://flutter.dev) (SDK ^3.13.0) & [Dart](https://dart.dev) |
| **State Management** | [Provider](https://pub.dev/packages/provider) with `ChangeNotifierProxyProvider` |
| **Cloud Backend & Auth** | [Supabase](https://supabase.com) (PostgreSQL Database, RLS, Auth) |
| **Local Offline Cache** | [Hive](https://pub.dev/packages/hive) & [Hive Flutter](https://pub.dev/packages/hive_flutter) |
| **Charts & Graphs** | [fl_chart](https://pub.dev/packages/fl_chart) |
| **Animations** | [flutter_animate](https://pub.dev/packages/flutter_animate) |
| **Notifications** | [flutter_local_notifications](https://pub.dev/packages/flutter_local_notifications) & [timezone](https://pub.dev/packages/timezone) |
| **Monetization** | [Google Mobile Ads SDK](https://pub.dev/packages/google_mobile_ads) (AdMob) |
| **Configuration** | [flutter_dotenv](https://pub.dev/packages/flutter_dotenv) |

---

## 🏛️ Architecture & Folder Structure

```
water_tracker/
├── android/                   # Native Android configuration & adaptive mipmaps
│   └── app/build.gradle.kts   # App ID: com.asif.watertracker (Target SDK 34+)
├── assets/                    # Static assets & brand graphics
│   └── images/                # app_icon.png, app_logo.png, human_water.jpg
├── legal/                     # Google Play compliance web center
│   ├── index.html             # Legal portal & account deletion interface
│   ├── privacy.html           # Official Privacy Policy
│   ├── terms.html             # Terms of Service & End User Agreement
│   └── styles.css             # Glassmorphism dark/light stylesheet
├── lib/
│   ├── models/                # Immutable domain entities (UserProfile, WaterEntry)
│   ├── providers/             # State holders (AuthProvider, WaterProvider, SettingsProvider, ThemeProvider)
│   ├── screens/               # Feature screens (Auth, Home, Analytics, Settings, Onboarding, Splash)
│   ├── services/              # Infrastructure (SupabaseService, HiveService, NotificationService)
│   ├── theme/                 # AppColors, typography tokens, light & dark themes
│   ├── widgets/               # Reusable UI widgets (WavePainter, QuickAdd, HydrationPill)
│   └── main.dart              # App bootstrap & provider composition
├── .env                       # Environment secrets (Supabase URL & anon key)
└── pubspec.yaml               # Package manifests & asset registrations
```

---

## 🚀 Getting Started

### 1. Prerequisites
Ensure you have the following installed on your development machine:
- [Flutter SDK](https://docs.flutter.dev/get-started/install) (`v3.13.0` or higher)
- [Android Studio](https://developer.android.com/studio) or [VS Code](https://code.visualstudio.com/) with Flutter extension
- Android SDK (API 34+ recommended)
- Java 17+

### 2. Installation
Clone the repository to your local machine:
```bash
git clone https://github.com/<your-username>/water_tracker.git
cd water_tracker
```

Install all required Flutter dependencies:
```bash
flutter pub get
```

### 3. Environment Configuration
Create a `.env` file in the project root directory with your Supabase credentials:
```env
SUPABASE_URL=https://ibhottyiyqmgxwffvmvx.supabase.co
SUPABASE_ANON_KEY=your_supabase_anon_key_here
```

### 4. Running the App
Run on a connected Android device or emulator:
```bash
flutter run
```

### 5. Building Release APK / App Bundle
Generate the release build for Google Play Console:
```bash
# Generate Split APKs
flutter build apk --release

# Generate Android App Bundle (.aab) for Play Store
flutter build appbundle --release
```

---

## ⚖️ Legal & Compliance

This repository includes a production-grade, Google Play 2026 Developer Policy compliant **Legal Center** located in [`legal/`](legal/):
- **Privacy Policy:** Transparent disclosures regarding user data collection, encrypted transit (TLS 1.3), and zero third-party sharing.
- **Data Safety:** Full adherence to Google Play Data Safety guidelines.
- **Account & Data Deletion:** In-app one-tap deletion flow as well as an automated web-based deletion request handler.

---

## 👨‍💻 Author

<div align="center">

### **MD ASIF HUSAIN**
*Lead Mobile Developer & Creator of Water Tracker*

🌐 **Website:** [dhtechnology.in](https://dhtechnology.in)  
📫 **Contact Email:** [dhtech800@gmail.com](mailto:dhtech800@gmail.com)  
🚀 **Project:** Water Tracker Mobile Application  
📍 **Application ID:** `com.asif.watertracker`

</div>

---

## 📄 License

Copyright &copy; 2026 **MD ASIF HUSAIN**. All rights reserved.  
Unauthorized copying, modification, distribution, or reproduction of any part of this software is strictly prohibited.
