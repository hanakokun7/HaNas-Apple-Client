# HaNas

[한국어](README.ko.md) | [日本語](README.ja.md)

HaNas is a native file management client for iOS and macOS, built with SwiftUI. Both platform apps are maintained in one Xcode project and use separate schemes.

## Features

- Browse and manage files and folders
- Upload and download files
- Preview supported media and documents
- Sign in to a HaNas server and manage your connection
- English, Korean, and Japanese localizations

Features and interface details may differ between the iOS and macOS apps.

## Requirements

- Xcode 26.1 or later
- Swift 5
- iOS 17.6 or later for iPhone and iPad
- macOS 14.6 or later
- Access to a running HaNas server

## Open and run

Open the Xcode project at the repository root:

```sh
open HaNas.xcodeproj
```

Choose a scheme and a suitable destination:

- **HaNas** — iOS app; select an iPhone or iPad simulator or device.
- **HaNas for Mac** — macOS app; select **My Mac**.

Configure signing in Xcode if you are running on a physical device, then use **Product > Run** or press `⌘R`.

## Build from the command line

```sh
xcodebuild -project HaNas.xcodeproj \
  -scheme HaNas \
  -destination 'generic/platform=iOS Simulator' \
  CODE_SIGNING_ALLOWED=NO build

xcodebuild -project HaNas.xcodeproj \
  -scheme 'HaNas for Mac' \
  -destination 'generic/platform=macOS' \
  CODE_SIGNING_ALLOWED=NO build
```

## Project layout

```text
.
├── HaNas.xcodeproj/   # Shared Xcode project and schemes
├── HaNas.plist        # iOS property list
├── iOS/               # iOS sources, assets, and localizations
└── macOS/             # macOS sources, assets, and localizations
```

## First launch

Launch either app, enter the URL of your HaNas server, and sign in or register with an account supported by that server.

