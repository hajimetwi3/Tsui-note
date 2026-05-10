# Tsui Note
ブラウザで動く、ごく軽量なテキストの書き場です。

---

## ウェブサイト版（Cloudflare Pages：PWA対応）

以下URLからご利用可能です。  
[https://tsuinote.pages.dev/](https://tsuinote.pages.dev/)  

## 注意事項  
- 本サービスは現状のまま提供されており、動作の保証はありません。利用によって生じた損害について、作成者は一切の責任を負いません。自己責任でご利用ください。
- 現在、外部からのプルリクエストは受け付けていません（This repository does not accept external pull requests.）

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
- note.comで記事を公開中です。  
  [https://note.com/hajimetwi3/n/nece01928dc72](https://note.com/hajimetwi3/n/nece01928dc72)

- Xでもアナウンスしています。  
  [https://x.com/hajimetwi3/status/2049029946711109731](https://x.com/hajimetwi3/status/2049029946711109731)

## 作者  

[Hajime Tsui](https://hajimetwi3.github.io/hajimetwi3/)  

---

## RELATED  

本アプリは Tsui series(静かな道具たち)の一つです。  
[https://hajimetwi3.github.io/hajimetwi3/Tsui-series/](https://hajimetwi3.github.io/hajimetwi3/Tsui-series/)  
