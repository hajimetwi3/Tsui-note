# Tsui Note
ブラウザで動く、ごく軽量なテキストの書き場です。
1 ウィンドウで 1 ファイル分のテキストを編集。
ファイルやフォルダの管理機能は持ちません。
ログイン不要、インストール不要、データの外部送信なし。
複数のことを書きたいときは、ヘッダの ⧉ ボタンで別ウィンドウを開いてください。
各ウィンドウの本文は独立、UI 設定（テーマ・フォントサイズ等）はウィンドウ間で共有されます。


---

## ウェブサイト版（Cloudflare Pages：PWA対応）  

以下URLからご利用可能です。  
[https://tsuinote.pages.dev/](https://tsuinote.pages.dev/)  

## ダウンロード版  

`tsui-note.html` をダウンロードし、お使いのブラウザで開いてください。
ローカルファイルとして開くだけで動作します。インストールは不要です。

## 機能

- ファイル読み込み / 書き出し（File System Access API があれば同じファイルへの上書き、なければダウンロード形式）
- 文字エンコーディング自動判定（UTF-8 / BOM 付き UTF-16LE / BOM 付き UTF-16BE / Shift_JIS / EUC-JP）
- 改行コード切替（LF / CRLF / CR）と BOM の有無切替
- 折り返し / 横スクロール切替
- フォントサイズ調整、Sys Font 4 段階（S / M / L / XL）
- 6 テーマ：calm（default）/ green / amber / red / pink / cyber
- 日本語 / English UI 切替（初回はブラウザ言語から自動判定）
- 同一オリジン内の別ウィンドウとの設定リアルタイム同期

## キーボードショートカット

- `Ctrl+S` / `Cmd+S`（macOS） 保存
- `Ctrl+Shift+S` / `Cmd+Shift+S`（macOS） 別名で保存
- `Tab` 半角スペース 2 つを挿入

## 注意事項  
- 本サービスは現状のまま提供されており、動作の保証はありません。利用によって生じた損害について、作成者は一切の責任を負いません。自己責任でご利用ください。
- 現在、外部からのプルリクエストは受け付けていません（This repository does not accept external pull requests.）

### 文字エンコーディングの扱い

UTF-8 / BOM 付き UTF-16LE / BOM 付き UTF-16BE / Shift_JIS / EUC-JP の自動判定で**読み込み**と**再読込**に対応していますが、**保存できる形式は UTF-8 / UTF-16LE / UTF-16BE のみ**です。
Shift_JIS / EUC-JP として開いたファイルを保存すると、UTF-8 へのフォールバックが発生し、保存前に確認ダイアログが表示されます。

自動判定は最善努力です。Shift_JIS と EUC-JP はバイト列が部分的に重なるため、短いファイルや判別が難しいケースでは誤判定されることがあります。文字化けして表示された場合は、フッターのエンコーディングピルから「(目的のエンコーディング) で再読込」を選んでください。

Firefox / Safari など File System Access API 非対応環境では再読込メニューを利用できません。
文字化けする場合は、Chrome / Edge など File System Access API 対応ブラウザで開いて再読込メニューを使うか、事前にファイルを UTF-8 に変換してください。

### 編集中の本文の永続化

編集中の本文や、開いたファイルへのハンドルは localStorage / IndexedDB に保存されません。
ウィンドウを閉じると編集中の内容は消えます。

## PRIVACY

ファイルや入力内容は、本アプリ本体から外部送信されません。
`connect-src 'none'` により、`fetch` 等のネットワーク送信は、ブラウザレベルで禁止されます。DevTools の Network タブで確認いただけます。

編集中の本文は localStorage や IndexedDB に保存されません。ウィンドウを閉じると消えます。保存したい内容はファイルに書き出してください。
UI 設定（Font / Wrap / Sys Font / Theme / Lang）は localStorage に保存され、同一オリジン内の別ウィンドウとリアルタイムに同期します。

本アプリ本体には計測機能は一切含まれていません（上記の `connect-src 'none'` により、ブラウザの CSP 機構で外部送信が禁止されるため）。

一方、作者プロフィールや Tsui series のランディングページ等の情報ページでは、訪問数の把握に Cloudflare Web Analytics を利用しています（Cookie なし / フィンガープリントなし / クロスサイトトラッキングなし）。

なお、別途プラットフォーム側（配信元サーバや中継事業者等）で計測・記録されている可能性はあります。

## ライセンス

[MIT License](LICENSE)

© 2026 Hajime Tsui

## Third-party

なし。外部モジュールには依存しません。  

---  

## アナウンス  
- X: [https://x.com/hajimetwi3/status/2053658377407086748](https://x.com/hajimetwi3/status/2053658377407086748)
- Note: [https://note.com/hajimetwi3/n/nd6ac4c75acc8](https://note.com/hajimetwi3/n/nd6ac4c75acc8)  

## 作者  

[Hajime Tsui](https://hajimetwi3.github.io/hajimetwi3/)  

---

## RELATED  

本アプリは Tsui series(静かな道具たち)の一つです。  
[https://hajimetwi3.github.io/hajimetwi3/Tsui-series/](https://hajimetwi3.github.io/hajimetwi3/Tsui-series/)  
