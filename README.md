# ToneDrill v2.0

小さなギター向け音楽学習アプリケーション（React + Vite）。
弦とフレットを入力すると、その音名を判定し、選択したキー（スケール）または設定したルート音からのインターバル（音程）を表示します。

## 主な機能

- 弦ごとのチューニング編集（デフォルト: 標準チューニング）
- モード選択: `SingleTone`（キー基準のスケール・インターバル） / `ChordTone`（指定したルートからのクロマティック・インターバル）
- 入力形式: `弦,フレット`（例: `6,3`）で音名とインターバルを確認
- シンプルな入力バリデーション（弦番号の存在確認、フレット範囲: 0–22）

## 主要ファイル

- アプリ本体: [src/App.jsx](src/App.jsx#L1-L400)
- 音理論定義: [src/constants.jsx](src/constants.jsx#L1-L500)
- エントリーポイント: [src/main.jsx](src/main.jsx#L1-L200)
- HTML: [index.html](index.html#L1-L50)
- ビルド設定: [vite.config.js](vite.config.js#L1-L50)
- スタイル: [src/App.css](src/App.css#L1-L50), [src/index.css](src/index.css#L1-L50)

## 開発: ローカルでの起動方法

依存をインストールして開発サーバを起動します。

```bash
npm install
npm run dev
```

開発中は Vite の HMR（ホットリロード）で変更が即時反映されます。

## 技術スタック

- フロントエンド: React 19 + Vite
- スタイリング: TailwindCSS（`@tailwindcss/vite`）
- 補助: `tailwind-variants`（UIユーティリティ）

## 改善案（短期）

- `弦` と `フレット` をそれぞれプルダウンやスピナーにして誤入力を減らす
- フレット上の音を図示するギターネック表示を追加
- フレット上限（現在22）を定数化して変更しやすくする（`src/constants.jsx`）

## 貢献

バグ修正やUI改善の PR を歓迎します。まず issue を開いてください。

---

更新: README をプロジェクトの実装に合わせて日本語で書き換えました。
