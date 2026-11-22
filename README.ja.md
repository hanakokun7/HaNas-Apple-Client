# HaNas

[English](README.md) | [한국어](README.ko.md)
HaNas は SwiftUI で開発された iOS および macOS 向けのネイティブなファイル管理アプリです。両プラットフォームのアプリは 1 つの Xcode プロジェクトで管理し、プラットフォームごとに異なるスキームでビルド・実行します。

## 主な機能

- ファイルやフォルダの閲覧と管理
- ファイルのアップロードとダウンロード
- 対応するメディアや書類のプレビュー
- HaNas サーバーへのログインと接続設定の管理
- 英語、韓国語、日本語のローカライズ

iOS アプリと macOS アプリでは、機能やインターフェースが一部異なる場合があります。

## 必要条件

- Xcode 26.1 以降
- Swift 5
- iPhone および iPad: iOS 17.6 以降
- macOS 14.6 以降
- 稼働中の HaNas サーバーへのアクセス

## 開いて実行する

リポジトリのルートにある Xcode プロジェクトを開きます。

```sh
open HaNas.xcodeproj
```

スキームと実行先を選択します。

- **HaNas** — iOS アプリ。iPhone または iPad のシミュレータかデバイスを選択します。
- **HaNas for Mac** — macOS アプリ。**My Mac** を選択します。

実機で実行する場合は Xcode で署名を設定し、**Product > Run** を選択するか `⌘R` を押します。

## コマンドラインからビルド

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

## プロジェクト構成

```text
.
├── HaNas.xcodeproj/   # 共通の Xcode プロジェクトとスキーム
├── HaNas.plist        # iOS のプロパティリスト
├── iOS/               # iOS のソース、アセット、ローカライズ
└── macOS/             # macOS のソース、アセット、ローカライズ
```

## 初回起動

アプリを起動し、HaNas サーバーの URL を入力して、そのサーバーで利用できるアカウントでログインまたは登録します。

