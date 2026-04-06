# StickerSmash

A universal mobile app built with React Native and Expo as part of the official [Expo Tutorial](https://docs.expo.dev/tutorial/introduction/). StickerSmash allows users to select a photo, place emoji stickers on it with drag-and-scale gestures, and save the final creation to their device.

> **Note:** This tutorial was completed using the iOS Simulator only. If you'd like to run the app on Android, you'll need to install [Android Studio](https://developer.android.com/studio), which includes the Android SDK and emulator. Once installed, press `a` in the Expo dev server terminal to launch the app on the Android emulator.

## Features

- Select a photo from your device's media library
- Browse and place emoji stickers on your photo
- Drag and scale stickers using touch gestures
- Capture a screenshot and save it to your device
- Cross-platform support for iOS, Android, and web

## Prerequisites

Before running this project, make sure you have the following installed:

- **Node.js** (LTS version recommended): install via [Homebrew](https://brew.sh/) on macOS: `brew install node`
- **Xcode**: install from the [Mac App Store](https://apps.apple.com/us/app/xcode/id497799835) (required for iOS Simulator)
  - After installing, open Xcode once to accept the license and install additional components
  - Install the **iOS Simulator** runtime when prompted during Xcode setup
- **Expo Go** (optional): install on a physical device from the App Store or Google Play to test on a real phone
- **Expo Orbit** (optional): a macOS menu bar app for managing simulators and builds

## Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/robertroddev/Expo-learning-project.git
   cd Expo-learning-project/StickerSmash
   ```

2. Install dependencies:

   ```bash
   npm install
   ```

## Running the App

Start the Expo development server:

```bash
npx expo start
```

Once the server is running, use the following keyboard shortcuts in the terminal:

- Press `i` to open the app in the **iOS Simulator**
- Press `w` to open the app in a **web browser**
- Press `a` to open the app on an **Android emulator** (requires Android Studio)
- Scan the QR code with **Expo Go** on a physical device

## Usage

1. Launch the app and tap **"Choose a photo"** to select an image from your library
2. Tap **"Use this photo"** to continue with the default background image
3. Once a photo is selected, use the toolbar to:
   - **Reset**: go back to the photo selection screen
   - **Add sticker**: open the emoji picker modal and select a sticker
   - **Save**: capture a screenshot and save it to your device
4. Interact with stickers using gestures:
   - **Drag**: tap and hold a sticker to move it anywhere on the photo
   - **Double-tap**: double-tap a sticker to enlarge it; double-tap again to return it to its original size
   - **Pinch**: use two fingers to scale a sticker up or down

## Tech Stack

- [Expo](https://expo.dev/) (SDK 54)
- [React Native](https://reactnative.dev/)
- [TypeScript](https://www.typescriptlang.org/)
- [Expo Router](https://docs.expo.dev/router/introduction/): file-based navigation
- [React Native Gesture Handler](https://docs.swmansion.com/react-native-gesture-handler/): touch gestures
- [React Native Reanimated](https://docs.swmansion.com/react-native-reanimated/): animations
- [expo-image-picker](https://docs.expo.dev/versions/latest/sdk/imagepicker/): media library access
- [expo-media-library](https://docs.expo.dev/versions/latest/sdk/media-library/): saving images to device
- [react-native-view-shot](https://github.com/gre/react-native-view-shot): screenshot capture (native)
- [dom-to-image](https://github.com/tsayen/dom-to-image): screenshot capture (web)

## Project Structure

```
StickerSmash/
├── app/
│   ├── (tabs)/
│   │   ├── _layout.tsx      # Tab navigation layout
│   │   ├── index.tsx         # Home screen (main app)
│   │   └── about.tsx         # About screen
│   ├── _layout.tsx           # Root layout with Stack navigator
│   └── +not-found.tsx        # 404 screen
├── assets/
│   └── images/               # App images, icons, and emoji stickers
├── components/
│   ├── Button.tsx             # Themed button component
│   ├── CircleButton.tsx       # Circular add-sticker button
│   ├── EmojiList.tsx          # Horizontal emoji selector
│   ├── EmojiPicker.tsx        # Bottom sheet emoji modal
│   ├── EmojiSticker.tsx       # Draggable/scalable sticker
│   ├── IconButton.tsx         # Icon + label button
│   └── ImageViewer.tsx        # Main image display
├── app.json                   # Expo configuration
├── package.json
└── tsconfig.json
```
