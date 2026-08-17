# Webポートフォリオ（案件獲得用LP）

上田誠一郎の業務改善パートナーサービス紹介用、1ページの静的サイトです。

## ファイル構成

- `index.html` … ページ本体
- `style.css` … デザイン（配色・レイアウト）
- `script.js` … モバイルメニュー、スクロール時のフェード表示
- `assets/profile.jpg` … プロフィール写真

## 公開前に必ずやること

### 1. お問い合わせフォームの送信先を設定する

`index.html` 内の以下の行を、実際のFormspreeのフォームIDに差し替えてください。

```html
<form class="contact-form blueprint-frame reveal" action="https://formspree.io/f/REPLACE_WITH_YOUR_FORM_ID" method="POST">
```

手順：
1. https://formspree.io で無料アカウントを作成（`s.u.business.260817@gmail.com` で登録）
2. 新しいフォームを作成し、表示された `https://formspree.io/f/xxxxxxx` のURLをコピー
3. 上記の `action` 属性の値を、コピーしたURLに置き換える
4. 公開後、テスト送信を1回行い、メールが届くか確認する（無料プランは月50件まで）

### 2. OGP画像のURLを絶対URLにする

`index.html` の `<meta property="og:image" content="assets/profile.jpg" />` は、SNSでシェアされたときの画像表示に使われます。GitHub Pages等で公開したら、実際のURL（例：`https://ユーザー名.github.io/リポジトリ名/assets/profile.jpg`）に書き換えると、シェア時に正しく画像が表示されます。

## 公開方法（GitHub Pages・無料）

1. GitHubでアカウントを作成し、新しいリポジトリを作成する
2. このフォルダの中身（`index.html`、`style.css`、`script.js`、`assets/`）をリポジトリにアップロードする
3. リポジトリの Settings → Pages で、公開ブランチを指定する
4. 数分後、`https://ユーザー名.github.io/リポジトリ名/` でサイトが公開される

独自ドメインを取得した場合は、同じPages設定画面でドメインを追加できます。

## 内容を後で編集したいとき

- 文章：`index.html` 内の日本語テキストを直接書き換える（HTMLタグは残したまま）
- 写真：`assets/profile.jpg` を新しい写真ファイルに差し替える（ファイル名は同じにする）
- 色：`style.css` の先頭 `:root { ... }` の中の色コード（`--accent` など）を変更する

## 動作確認済みの環境

- デスクトップ／モバイルのレスポンシブ表示
- ライトモード／ダークモード（OSの設定に自動追従）
- モバイルのハンバーガーメニュー
- キーボード操作・フォーカス表示
