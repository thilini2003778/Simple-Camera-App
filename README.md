# Simple-Camera-App

**Course:** Mobile Application Development – Assignment  
**Student:** M. Thilini Kanchana  
**Technology:** Android Studio, Kotlin, Jetpack Compose (Material 3)

---

## 📌 Project Overview
A native Android application developed using **Kotlin** and **Jetpack Compose** that demonstrates camera access, runtime permissions, image capture, preview rendering, and system-level sharing via Android Intents and `FileProvider`.

---

## ✨ Features
1. **Camera Permissions**: Dynamically checks and requests the `android.permission.CAMERA` runtime permission with informative feedback.
2. **Camera Access & Photo Capture**: Launches the device's system camera application using `ActivityResultContracts.TakePicturePreview()`.
3. **Photo Display**: Renders the captured photograph inside a styled Material 3 Card with placeholder state and smooth aspect ratio handling.
4. **Photo Retake Option**: Allows taking multiple photos with dynamic button state update ("Open Camera" / "Retake Photo").
5. **System Sharing Interface**: Includes a dedicated "Share Photo" button that invokes Android's native sharing sheet (`Intent.ACTION_SEND` wrapped in `Intent.createChooser()`) to share captured photos across installed apps (e.g., Bluetooth, WhatsApp, Gmail, Quick Share).

---

## 🔑 Key Concepts & Architecture
- **Runtime Permissions**: `rememberLauncherForActivityResult(ActivityResultContracts.RequestPermission())`
- **Camera Access & Result Callback**: `rememberLauncherForActivityResult(ActivityResultContracts.TakePicturePreview())`
- **Intents & Content URIs**: Secure file sharing using AndroidX `FileProvider` (`res/xml/file_paths.xml`) to prevent `FileUriExposedException`
- **Jetpack Compose Material 3**: `Scaffold`, `TopAppBar`, `Surface`, `Card`, and theme responsiveness for Light and Dark modes.

---

## 🚀 How to Run
1. Open the project in **Android Studio**.
2. Let Gradle sync dependencies.
3. Run on an Android Virtual Device (AVD) or physical device running Android 7.0 (API level 24) or higher.
4. Tap **Open Camera**, grant camera permission if requested, capture a photo, and tap **Share Photo** to test sharing.
