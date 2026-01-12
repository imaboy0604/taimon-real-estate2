---
name: ベガハウス風デザイン刷新ロードマップ
overview: ベガハウスを参考にしたミニマルで清潔感のある不動産サイトへの刷新を、5つのフェーズに分けて段階的に実装する計画
todos:
  - id: phase1-tokens
    content: デザイントークンファイル作成（カラー、タイポグラフィ、スペーシング）
    status: completed
  - id: phase1-global
    content: グローバルスタイルの更新（リセット、ベースライン、フォント最適化）
    status: completed
  - id: phase1-fonts
    content: フォント設定の最適化（縦書き対応フォント追加）
    status: completed
  - id: phase2-header
    content: Headerコンポーネントの新規作成（固定ヘッダー、ナビゲーション）
    status: completed
  - id: phase2-hero
    content: HeroSectionの修正（ヘッダー分離、メインビジュアル調整）
    status: completed
  - id: phase3-hero-rebuild
    content: HeroSectionの再構築（フルスクリーンビジュアル、タイトル配置）
    status: pending
  - id: phase3-concept
    content: ConceptSectionの新規作成（縦書きテキスト、大きな余白）
    status: pending
  - id: phase4-gallery
    content: ExampleGalleryの新規作成（グリッドレイアウト、ホバーエフェクト）
    status: pending
  - id: phase4-youtube
    content: YouTubeSectionの新規作成（動画埋め込み、レスポンシブ）
    status: pending
  - id: phase4-quicklinks
    content: QuickLinksSectionの新規作成（4カラムのコンテンツナビゲーション）
    status: pending
  - id: phase4-cta
    content: CTASectionの新規作成（メディア向け・採用情報ボタン）
    status: pending
  - id: phase4-contactbar
    content: ContactBarの新規作成（ダークグレーのコンタクトバー）
    status: pending
  - id: phase4-social
    content: SocialLinksの新規作成（3カラムSNSカード、グラデーションオーバーレイ）
    status: pending
  - id: phase4-staff
    content: StaffSectionの新規作成（2カラム、画像左、縦書きテキスト右）
    status: pending
  - id: phase4-qa
    content: QASectionの新規作成（2カラム、画像左、縦書きテキスト右）
    status: pending
  - id: phase4-blog
    content: StaffBlogSectionの新規作成（3カラムグリッド、ラベル、縦書きテキスト）
    status: pending
  - id: phase4-existing
    content: 既存コンポーネントのスタイル統一と調整
    status: pending
  - id: phase5-footer
    content: Footerの再設計（シンプルなレイアウト、グリッド）
    status: pending
  - id: phase5-responsive
    content: 全コンポーネントのレスポンシブ対応（モバイル・タブレット）
    status: pending
  - id: phase5-performance
    content: パフォーマンス最適化（画像、フォント、CSS）
    status: pending
---

# ベガハウス風デザイン刷新ロードマップ

## プロジェクト構造の分析

### 現在の構造

- **フレームワーク**: Svelte + Vite
- **主要コンポーネント**: `HeroSection`, `FeaturesSection`, `StoreSection`, `Features2Section`, `Features3Section`, `FAQSection`, `Footer`
- **スタイル**: `styles.css`（グローバル）+ 各コンポーネント内の`<style>`タグ

### 修正・新規作成が必要なファイル

**修正が必要なファイル:**

- `src/components/HeroSection.svelte` - メインビジュアルとヘッダーの再構築
- `src/components/Footer.svelte` - フッターの再設計
- `styles.css` - グローバルスタイルとデザインシステムの刷新
- `index.html` - フォント読み込みの最適化
- `src/App.svelte` - コンポーネント構成の見直し

**新規作成が必要なファイル:**

- `src/components/Header.svelte` - 独立したヘッダーコンポーネント（最小限のナビゲーション、パジネーションドット）
- `src/components/ConceptSection.svelte` - コンセプト・導入テキストエリア（縦書き対応、地図オーバーレイ）
- `src/components/QuickLinksSection.svelte` - 4 カラムのコンテンツナビゲーション（「家づくりの特徴」「そうまち」「実例集」「スタッフブログ」）
- `src/components/CTASection.svelte` - CTA ボタンセクション（「メディアの皆様へ」「RECRUIT」）
- `src/components/ContactBar.svelte` - コンタクトバー（ダークグレー、会社名と電話番号）
- `src/components/ExampleGallery.svelte` - 実例集グリッド（アダプティブ 4 列 →3 列、縦書きタイトル）
- `src/components/YouTubeSection.svelte` - YouTube 動画セクション（2x2 グリッド、オーバーレイテキスト、VEGA HOUSE ロゴ）
- `src/components/SocialLinks.svelte` - SNS セクション（3 カラムカード、グラデーションオーバーレイ、背景画像）
- `src/components/StaffSection.svelte` - スタッフ紹介セクション（2 カラム、画像左、縦書きテキスト右、番号アイコン）
- `src/components/QASection.svelte` - Q&A セクション（2 カラム、画像左、縦書きテキスト右、番号アイコン）
- `src/components/StaffBlogSection.svelte` - スタッフブログセクション（3 カラムグリッド、ラベル、縦書きテキスト、日付）
- `src/styles/design-tokens.css` - デザイントークン（カラー、タイポグラフィ、スペーシング）

---

## フェーズ別実装計画

### フェーズ 1: 全体の共通設定（デザインシステム構築）

**目標**: 清潔感と高級感を表現するデザイントークンの確立

**作業内容:**

1. **デザイントークンファイル作成** (`src/styles/design-tokens.css`)

- カラーパレット: 白基調、アクセントカラー（控えめなグレー、ベージュ系）
- タイポグラフィ: 明朝体（縦書き対応）+ ゴシック体（本文）
- スペーシングシステム: 8px 基準のグリッド（8, 16, 24, 32, 48, 64, 96, 128px）
- ブレークポイント: mobile(768px), tablet(1024px), desktop(1440px)

2. **グローバルスタイル更新** (`styles.css`)

- リセット CSS の最適化
- ベースラインの統一（line-height: 1.6-1.8）
- フォントレンダリングの最適化（-webkit-font-smoothing, text-rendering）

3. **フォント設定** (`index.html`)

- 縦書き対応フォントの追加（Noto Serif JP, 游明朝等）
- フォント読み込みの最適化（preload, display: swap）

**デザインの要点:**

- 余白: セクション間は 96-128px、要素間は 24-48px
- フォントサイズ: 見出し（32-48px）、本文（16-18px）、キャプション（14px）
- カラー: 背景は純白（#FFFFFF）、テキストは濃いグレー（#1A1A1A）、アクセントは控えめ

---

### フェーズ 2: ヘッダーとナビゲーションの再構築

**目標**: シンプルで機能的な固定ヘッダーの実装

**作業内容:**

1. **新規コンポーネント作成** (`src/components/Header.svelte`)

- 最小限のトップバー（固定または通常）
- 左側: 小さなアイコンまたはテキスト（例: 「お家を想像します。」）
- 右側: 小さなテキスト（例: 「5 年目)」）
- 中央: パジネーションドット（6 個、カルーセル用、現在のページを表示）
- 背景: 透明または半透明の白
- ハンバーガーメニュー（モバイル対応、必要に応じて）

2. **HeroSection の修正**

- ヘッダー部分を`Header.svelte`に分離
- メインビジュアル部分のみを残す
- パディング調整（ヘッダー分の余白を考慮）

**デザインの要点:**

- ヘッダー高さ: 64-80px
- 背景: 半透明の白（rgba(255, 255, 255, 0.95)）+ backdrop-filter: blur(10px)
- ナビゲーション: フォントサイズ 16px、間隔 24-32px
- ホバーエフェクト: 控えめなアンダーラインまたは色変化

---

### フェーズ 3: メインビジュアルとコンセプトエリア

**目標**: 縦書きテキストを活用した印象的な導入セクション

**作業内容:**

1. **HeroSection の再構築**

- フルスクリーンまたは大きなビジュアルエリア
- 左側: 縦書きの日本語テキスト
- メインタイトル「鹿児島の 暮らしを 建てる工務店 ベガハウス」（大きな太字、明朝体）
- 説明文（複数段落、縦書き）
- 右側: 大きな高品質画像（インテリア、中庭、自然光）
- 英語テキストのオーバーレイ（右下）
- 地図のオーバーレイ（日本または九州地方、鹿児島をマーク）
- パジネーションドット（6 個、現在のページを表示）

2. **新規コンポーネント作成** (`src/components/ConceptSection.svelte`)

- 縦書きテキストの実装
- CSS: `writing-mode: vertical-rl`（右から左）
- フォント: 明朝体（Noto Serif JP, 游明朝）
- 大きな余白を取ったレイアウト（左右 96-128px、上下 64-96px）
- テキストのアニメーション（フェードイン、スクロール連動）
- 地図オーバーレイの実装（SVG または画像、半透明）

**デザインの要点:**

- 縦書きテキスト: フォントサイズ 24-32px、行間 1.8-2.0
- 余白: 左右に 96-128px、上下に 64-96px
- 背景: 白または非常に薄いグレー（#FAFAFA）
- テキストカラー: 濃いグレー（#1A1A1A）または黒（#000000）

---

### フェーズ 4: 各コンテンツセクション

**目標**: 統一感のあるグリッドレイアウトの実装

**作業内容:**

1. **実例集グリッド** (`src/components/ExampleGallery.svelte`)

- 3 カラムまたは 4 カラムのグリッド
- 画像のアスペクト比統一（例: 4:3 または 16:9）
- ホバーエフェクト（拡大、オーバーレイ）
- 画像の遅延読み込み

2. **YouTube セクション** (`src/components/YouTubeSection.svelte`)

- 動画の埋め込み（16:9 のアスペクト比）
- レスポンシブ対応（max-width: 1200px）
- セクションタイトルと説明文

3. **SNS リンク** (`src/components/SocialLinks.svelte`)

- アイコンの配置（横並び、間隔 24-32px）
- ホバーエフェクト（色変化、拡大）
- SVG アイコンの使用

4. **既存コンポーネントの調整**

- `FeaturesSection`, `Features2Section`, `Features3Section`のスタイル統一
- グリッドレイアウトの最適化
- 余白の統一

**デザインの要点:**

- グリッド間隔: 24-32px（gap）
- カード: 角丸 8-12px、影は控えめ（0 2px 8px rgba(0,0,0,0.08)）
- 画像: object-fit: cover、transition: transform 0.3s ease
- セクション間: 96-128px の余白

---

### フェーズ 5: フッターとレスポンシブ調整

**目標**: 完全なレスポンシブ対応とフッターの最適化

**作業内容:**

1. **フッターの再設計** (`src/components/Footer.svelte`)

- 左側: 「VEGA HOUSE」ロゴ、会社名、住所、電話、FAX、メールアドレス
- 右側: パートナーロゴのグリッド（2x3、モノクロまたはデサチュレート）
- 下部: 細い横線、ナビゲーションリンク（「会社概要」「FAQ/お支払い方法」「プライバシーポリシー」など）、コピーライト（右端）
- 背景: 薄いグレー（#F7F7F7）
- グリッドレイアウト（デスクトップ: 2 カラム、モバイル: 1 カラム）

2. **レスポンシブ対応**

- 全コンポーネントのモバイル最適化
- ブレークポイント: 768px, 1024px, 1440px
- フォントサイズの調整（clamp 関数の活用）
- 余白の調整（モバイル: 16-24px、デスクトップ: 32-48px）

3. **パフォーマンス最適化**

- 画像の最適化（WebP 形式、遅延読み込み）
- フォントの最適化（subset、preload）
- CSS の最適化（不要なスタイルの削除）

**デザインの要点:**

- モバイル: フォントサイズ 14-16px、余白 16-24px
- タブレット: フォントサイズ 16-18px、余白 24-32px
- デスクトップ: フォントサイズ 18-20px、余白 32-48px
- 縦書きテキスト: モバイルでは横書きに変更（writing-mode: horizontal-tb）

---

## デザインの要点まとめ

### 清潔感と高級感を出すための CSS ポイント

1. **余白の取り方**

- セクション間: 96-128px（デスクトップ）、64-96px（モバイル）
- 要素間: 24-48px
- コンテナの最大幅: 1200-1440px、パディング: 32-48px

2. **タイポグラフィ**

- 見出し: 32-48px（明朝体）、行間 1.4-1.6
- 本文: 16-18px（ゴシック体）、行間 1.6-1.8
- 文字間隔: 0.02-0.05em
- フォントレンダリング: -webkit-font-smoothing: antialiased

3. **カラーパレット**

- 背景: #FFFFFF（純白）
- テキスト: #1A1A1A（濃いグレー）
- アクセント: #8B7355（ベージュ系）または #6B6B6B（グレー）
- ボーダー: #E5E5E5（薄いグレー）

4. **影とエフェクト**

- ボックスシャドウ: 控えめ（0 2px 8px rgba(0,0,0,0.08)）
- ホバーエフェクト: 軽い拡大（transform: scale(1.02)）または色変化
- トランジション: 0.3s ease

5. **縦書きテキスト**

- writing-mode: vertical-rl（右から左）
- text-orientation: upright（文字の向き）
- フォント: 明朝体（Noto Serif JP 等）

---

## 実装の優先順位

1. **最優先**: フェーズ 1（デザインシステム）→ フェーズ 2（ヘッダー）
2. **次**: フェーズ 3（メインビジュアル・コンセプト）
3. **その後**: フェーズ 4（コンテンツセクション）
4. **最後**: フェーズ 5（フッター・レスポンシブ）

各フェーズは独立して実装可能ですが、フェーズ 1 のデザインシステムは他のフェーズの基盤となるため、最初に完了させることを推奨します。
