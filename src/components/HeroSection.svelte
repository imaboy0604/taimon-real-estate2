<section class="hero-section">
  <div class="overlay-top"></div>
  <div class="overlay-bottom"></div>

  <div class="hero-content">
    <h1 class="hero-title">
      より快適に。<br />
      より上質に。
    </h1>
    <p class="hero-subtitle">あなたの住まい探しを、より特別な体験に。</p>
    <div class="hero-logo">
      <img src="/images/logo1.jpg" alt="タイモン不動産" class="logo1-image" />
    </div>
  </div>
</section>

<style>
  /* ============================================
     ロゴサイズの微調整用CSS変数（最適化済み）
     ============================================ */
  :global(.hero-section) {
    --logo-nav-height: 40px; /* ナビゲーションバーのロゴ高さ */
    --logo-hero-max-width: 220px; /* ヒーローセクションのロゴ最大幅（縮小） */
    --logo-hero-max-width-mobile: 180px; /* モバイル時のロゴ最大幅 */
  }

  .hero-section {
    position: relative;
    width: 100%;
    min-height: 100vh;
    /* 既存画像を使用 - 写真がくっきり見えるように */
    background: url("/images/gallery-1.jpg") center/cover no-repeat;
    background-size: cover;
    background-attachment: fixed;
    background-position: center top;
    display: flex;
    flex-direction: column;
    color: white;
    overflow: hidden;
    /* ヘッダー分の余白を考慮 */
    padding-top: 80px;
  }

  .overlay-top {
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background: transparent;
    z-index: 1;
  }

  .overlay-bottom {
    position: absolute;
    bottom: 0;
    left: 0;
    right: 0;
    height: 120px;
    background: white;
    z-index: 2;
    clip-path: polygon(0 40%, 100% 0%, 100% 100%, 0% 100%);
    animation: waveClip 10s ease-in-out infinite;
  }
  
  /* 波打つようなアクション - clip-pathで波の形をアニメーション */
  @keyframes waveClip {
    0%, 100% {
      clip-path: polygon(0 40%, 100% 0%, 100% 100%, 0% 100%);
    }
    25% {
      clip-path: polygon(0 35%, 100% 5%, 100% 100%, 0% 100%);
    }
    50% {
      clip-path: polygon(0 45%, 100% -5%, 100% 100%, 0% 100%);
    }
    75% {
      clip-path: polygon(0 35%, 100% 5%, 100% 100%, 0% 100%);
    }
  }
  
  /* より滑らかな波の効果 - グラデーションオーバーレイ */
  .overlay-bottom::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    height: 100%;
    background: linear-gradient(
      180deg,
      rgba(255, 255, 255, 0) 0%,
      rgba(255, 255, 255, 0.3) 30%,
      rgba(255, 255, 255, 0.7) 60%,
      rgba(255, 255, 255, 1) 100%
    );
    animation: waveGradient 12s ease-in-out infinite;
  }
  
  @keyframes waveGradient {
    0%, 100% {
      transform: translateY(0);
    }
    50% {
      transform: translateY(-5px);
    }
  }


  .hero-content {
    position: relative;
    z-index: 10;
    flex: 1;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    gap: 24px;
    padding: 0;
    text-align: center;
    width: 100%;
    min-height: 100vh;
    margin: 0;
  }

  .hero-title {
    font-family: var(--font-family-serif, 'Noto Serif JP', 'Yu Mincho', '游明朝', serif);
    font-size: clamp(32px, 8vw, 72px);
    font-weight: 500;
    line-height: var(--line-height-tight, 1.4);
    letter-spacing: var(--letter-spacing-heading-large, 0.1em);
    max-width: 90%;
    color: white;
    text-shadow: 2px 2px 8px rgba(0, 0, 0, 0.5);
  }

  .hero-subtitle {
    font-family: var(--font-family-serif, 'Noto Serif JP', 'Yu Mincho', '游明朝', serif);
    font-size: clamp(16px, 2.5vw, 18px);
    font-weight: 400;
    line-height: var(--line-height-relaxed, 1.8);
    letter-spacing: var(--letter-spacing-body-wide, 0.05em);
    color: white;
    opacity: 1;
    max-width: 90%;
    text-shadow: 1px 1px 4px rgba(0, 0, 0, 0.5);
    margin-bottom: 40px;
  }

  .hero-logo {
    margin-top: 40px;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .logo1-image {
    max-width: var(--logo-hero-max-width, 220px);
    width: 100%;
    height: auto;
    object-fit: contain;
    filter: drop-shadow(2px 2px 6px rgba(0, 0, 0, 0.4));
    /* 白色背景を透過させる - darkenモードで白色を透明化 */
    mix-blend-mode: darken;
  }

  @media (max-width: 1024px) {
    .hero-section {
      background-attachment: scroll;
      padding-top: 60px;
    }
  }

  @media (max-width: 768px) {
    .hero-section {
      min-height: 100vh;
      background-attachment: scroll;
      padding-top: 50px;
    }

    .hero-content {
      padding: 0;
      min-height: 100vh;
    }

    .hero-title {
      font-size: clamp(28px, 10vw, 44px);
      padding: 0 20px;
    }

    .hero-subtitle {
      font-size: clamp(14px, 4vw, 18px);
      padding: 0 20px;
    }

    .logo1-image {
      max-width: var(--logo-hero-max-width-mobile, 180px);
    }
  }

  @media (max-width: 480px) {
    .hero-title {
      padding: 0 16px;
    }

    .hero-subtitle {
      padding: 0 16px;
    }
  }
</style>
