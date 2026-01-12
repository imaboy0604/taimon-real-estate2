<script>
  let menuOpen = false;

  function toggleMenu() {
    menuOpen = !menuOpen;
  }
</script>

<section class="hero-section">
  <div class="overlay-top"></div>
  <div class="overlay-bottom"></div>

  <nav class="navbar">
    <div class="navbar-content">
      <button class="menu-button" on:click={toggleMenu}>
        <svg
          width="20"
          height="20"
          viewBox="0 0 20 20"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            d="M2.5 5H17.5M2.5 10H17.5M2.5 15H17.5"
            stroke="currentColor"
            stroke-width="1.5"
            stroke-linecap="round"
          />
        </svg>
        <span>メニュー</span>
      </button>

      <div class="logo">
        <img src="/images/logo2.jpg" alt="タイモン不動産" class="logo-image" />
      </div>

      <div class="nav-links">
        <a href="#contact">お問い合わせ</a>
        <a href="#about">私たちについて</a>
      </div>
    </div>
  </nav>

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
    background: url("/images/gallery-1.jpg") center/cover no-repeat;
    background-size: cover;
    background-attachment: fixed;
    background-position: center top;
    display: flex;
    flex-direction: column;
    color: white;
    overflow: hidden;
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
    height: 100px;
    background: linear-gradient(
      180deg,
      rgba(255, 255, 255, 0) 0%,
      rgba(255, 255, 255, 1) 100%
    );
    clip-path: polygon(0 40%, 100% 0%, 100% 100%, 0% 100%);
    z-index: 2;
  }

  .navbar {
    position: relative;
    z-index: 10;
    padding: 0;
    width: 100%;
  }

  .navbar-content {
    display: grid;
    grid-template-columns: 1fr auto 1fr;
    align-items: center;
    width: 100%;
    max-width: 100%;
    margin: 0;
    padding: 20px;
  }

  .navbar-content > :first-child {
    justify-self: start;
  }

  .navbar-content > .logo {
    justify-self: center;
    flex: none;
  }

  .navbar-content > :last-child {
    justify-self: end;
  }

  .menu-button {
    display: flex;
    align-items: center;
    gap: 8px;
    padding: 8px 18px;
    background: white;
    border: none;
    border-radius: 25px;
    cursor: pointer;
    font-family: "Noto Serif JP", "Shippori Mincho", "Meiryo UI",
      "Hiragino Kaku Gothic ProN", "Hiragino Sans", sans-serif;
    font-size: 16px;
    font-weight: 500;
    color: #12161d;
  }

  .logo {
    flex: 1;
    display: flex;
    justify-content: center;
  }

  .logo-image {
    height: var(--logo-nav-height, 40px);
    width: auto;
    max-width: 180px;
    object-fit: contain;
    /* 白色背景を透過させる - darkenモードで白色を透明化 */
    mix-blend-mode: darken;
    filter: contrast(1.05) brightness(1.02);
  }

  .nav-links {
    display: flex;
    gap: 24px;
  }

  .nav-links a {
    font-family: "Noto Serif JP", "Shippori Mincho", "Meiryo UI",
      "Hiragino Kaku Gothic ProN", "Hiragino Sans", sans-serif;
    font-size: 16px;
    font-weight: 500;
    color: white;
    text-decoration: none;
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
    font-family: "Noto Serif JP", "Shippori Mincho", "Meiryo UI",
      "Hiragino Kaku Gothic ProN", "Hiragino Sans", sans-serif;
    font-size: clamp(32px, 8vw, 72px);
    font-weight: 500;
    line-height: 1.11;
    letter-spacing: -0.025em;
    max-width: 90%;
    text-shadow: 2px 2px 8px rgba(0, 0, 0, 0.5);
  }

  .hero-subtitle {
    font-family: "Noto Serif JP", "Shippori Mincho", "Meiryo UI",
      "Hiragino Kaku Gothic ProN", "Hiragino Sans", sans-serif;
    font-size: clamp(16px, 2.5vw, 18px);
    font-weight: 400;
    line-height: 1.44;
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
    }

    .navbar-content {
      padding: 16px;
    }
  }

  @media (max-width: 768px) {
    .hero-section {
      min-height: 100vh;
      background-attachment: scroll;
    }

    .navbar-content {
      padding: 12px 16px;
      gap: 0;
    }

    .menu-button {
      padding: 8px 14px;
      font-size: 14px;
    }

    .nav-links {
      display: none;
    }

    .logo-image {
      height: calc(var(--logo-nav-height, 40px) * 0.85);
      max-width: 140px;
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
