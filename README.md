# タイモン不動産 - Svelte Webサイト

Figmaデザインに基づいて実装された不動産サイトのSvelteコンポーネントです。

## セットアップ

### 必要な環境
- Node.js 18以上
- npm または yarn

### インストール

```bash
npm install
```

### 開発サーバーの起動

```bash
npm run dev
```

ブラウザで `http://localhost:5173` を開いて確認できます。

### ビルド

```bash
npm run build
```

### プレビュー

```bash
npm run preview
```

## プロジェクト構造

```
taimon-real-estate/
├── src/
│   ├── components/
│   │   ├── HeroSection.svelte      # ヒーローセクション
│   │   ├── FeaturesSection.svelte  # 特徴セクション
│   │   ├── Gallery.svelte          # ギャラリー
│   │   ├── Features2Section.svelte # 特徴2セクション
│   │   ├── Features3Section.svelte # 特徴3セクション
│   │   ├── FAQSection.svelte       # FAQセクション
│   │   └── Footer.svelte           # フッター
│   ├── App.svelte                  # メインアプリケーション
│   └── main.js                     # エントリーポイント
├── index.html
├── package.json
├── vite.config.js
└── svelte.config.js
```

## コンポーネント説明

### HeroSection
メインビジュアルとナビゲーションバーを含むヒーローセクション

### FeaturesSection
不動産の特徴と統計情報を表示するセクション

### Gallery
物件の画像ギャラリー

### Features2Section
3つの主要な特徴（立地、デザイン、セキュリティ）を表示

### Features3Section
「理想の住まいを見つける」セクション

### FAQSection
よくある質問のアコーディオン形式のセクション

### Footer
フッター情報とリンク

## デザイン仕様

- **フォント**: Inter Display
- **カラーパレット**: 
  - テキスト: #12161D (Neutral/900)
  - セカンダリテキスト: #61656E (Neutral/600)
  - 背景: #FFFFFF (Neutral/0)
  - フッター背景: #FAFAFB (Neutral/25)
  - ボーダー: #E5E5E6 (Neutral/100)

## レスポンシブデザイン

モバイル、タブレット、デスクトップに対応しています。
