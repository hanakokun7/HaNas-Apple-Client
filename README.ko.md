# HaNas

[English](README.md) | [日本語](README.ja.md)

HaNas는 SwiftUI로 만든 iOS 및 macOS용 네이티브 파일 관리 앱입니다. 두 플랫폼 앱은 하나의 Xcode 프로젝트에서 관리하며, 플랫폼별 스킴으로 빌드하고 실행합니다.

## 주요 기능

- 파일 및 폴더 탐색과 관리
- 파일 업로드 및 다운로드
- 지원되는 미디어와 문서 미리 보기
- HaNas 서버 로그인 및 연결 설정 관리
- 영어, 한국어, 일본어 현지화

iOS 앱과 macOS 앱의 기능 및 인터페이스는 일부 다를 수 있습니다.

## 요구 사항

- Xcode 26.1 이상
- Swift 5
- iPhone 및 iPad: iOS 17.6 이상
- macOS 14.6 이상
- 실행 중인 HaNas 서버에 접속 가능해야 합니다.

## 열기 및 실행

저장소 최상위의 Xcode 프로젝트를 엽니다.

```sh
open HaNas.xcodeproj
```

스킴과 실행 대상을 선택합니다.

- **HaNas** — iOS 앱. iPhone 또는 iPad 시뮬레이터나 기기를 선택합니다.
- **HaNas for Mac** — macOS 앱. **My Mac**을 선택합니다.

실제 기기에서 실행할 경우 Xcode에서 서명을 설정한 다음 **Product > Run**을 선택하거나 `⌘R`을 누릅니다.

## 명령줄에서 빌드

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

## 프로젝트 구조

```text
.
├── HaNas.xcodeproj/   # 공용 Xcode 프로젝트 및 스킴
├── HaNas.plist        # iOS 프로퍼티 목록
├── iOS/               # iOS 소스, 에셋, 현지화 파일
└── macOS/             # macOS 소스, 에셋, 현지화 파일
```

## 첫 실행

앱을 실행하고 HaNas 서버 주소를 입력한 뒤, 해당 서버에서 사용할 수 있는 계정으로 로그인하거나 가입합니다.

