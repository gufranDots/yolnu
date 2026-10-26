# Yolnu

Expo app for the **Working with Yolŋu Card** — a cultural competency recognition system guided by Yolŋu leadership in East Arnhem Land.

The app helps people learn about the card, complete onboarding, browse guest resources, and (as a member) manage a profile, view their card, and apply or renew.

Public information is based on [workingwithyolngu.com.au](https://www.workingwithyolngu.com.au/).

## Features

- **Onboarding** — card purpose, cultural competency stages, training, East Arnhem communities, and news
- **Guest access** — cultural competency framework, recognised training providers, community map, and news sources
- **Auth (demo)** — sign up, login, forgot/reset password, and email verification
- **Member area** — profile, view card, apply/renew, messages, and application status
- **Web and native** — iOS, Android, and web (web uses a phone frame for guest/map flows)

## Stack

- Expo SDK 57, React Native 0.86, React 19
- React Navigation (native stack + bottom tabs)
- TypeScript and JavaScript
- Async Storage, Expo Image Picker, React Native Maps, WebView

## Prerequisites

- Node.js 20+
- npm
- [Expo Go](https://expo.dev/go) or Xcode / Android Studio for device builds

## Setup

```bash
git clone https://github.com/gufranDots/yolnu.git
cd yolnu
npm install
```

For iOS native builds:

```bash
npm run pod
```

## Run

```bash
npm start          # Expo Dev Server
npm run ios        # iOS
npm run android    # Android
npm run web        # Web
```

Export a static web build:

```bash
npm run export:web
```

## Project layout

```
App.js                 # Root providers and app shell
src/context/           # Auth and demo state
src/navigation/        # Auth, guest, and member navigators
src/screens/           # Onboarding, auth, guest, and member screens
src/components/        # UI, layout, application, and card components
src/data/              # Onboarding, guest tiles, mock member data
src/theme/             # Colours, typography, and spacing
```

Auth and member flows currently use local demo state (no production backend).
