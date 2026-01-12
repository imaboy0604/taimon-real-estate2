<section class="footer-section">
  <div class="container">
    <div class="content">
      <div class="brand-section">
        <div class="logo-section">
          <div class="logo">
            <svg width="137" height="32" viewBox="0 0 137 32" fill="none" xmlns="http://www.w3.org/2000/svg">
              <text x="0" y="22" font-family="Shippori Mincho, Meiryo UI, Hiragino Kaku Gothic ProN, Hiragino Sans" font-size="24" font-weight="500" fill="#12161D">タイモン不動産</text>
            </svg>
          </div>
          <p class="tagline">
            より快適に。<br />
            より上質に。
          </p>
        </div>
      </div>

      <div class="links-section">
        <div class="links-column">
          <h3 class="column-title">サービス</h3>
          <div class="links">
            <a href="#features">物件紹介</a>
            <a href="#integrations">資金計画</a>
            <a href="#pricing">価格情報</a>
          </div>
        </div>

        <div class="links-column">
          <h3 class="column-title">会社情報</h3>
          <div class="links">
            <a href="#about">私たちについて</a>
            <a href="#blog">お知らせ</a>
            <a href="#careers">採用情報</a>
            <a href="#customers">お客様の声</a>
            <a href="#brand">ブランド</a>
          </div>
        </div>

        <div class="links-column">
          <h3 class="column-title">その他</h3>
          <div class="links">
            <a href="#community">コミュニティ</a>
            <a href="#contact">お問い合わせ</a>
            <a href="#dpa">個人情報保護</a>
            <a href="#terms">利用規約</a>
          </div>
        </div>
      </div>
    </div>

    <div class="divider"></div>

    <div class="footer-bottom">
      <p class="copyright">© 2024 タイモン不動産. All rights reserved</p>
      <div class="legal-links">
        <a href="#terms">利用規約</a>
        <a href="#policy">プライバシーポリシー</a>
        <a href="#cookie">Cookieポリシー</a>
        <a href="#partners">パートナー</a>
      </div>
    </div>
  </div>
</section>

<style>
  .footer-section {
    position: relative;
    background: url('/images/gallery-3.jpg') center/cover;
    padding: 80px 80px 40px;
    overflow: hidden;
    clip-path: polygon(0 0%, 100% 10%, 100% 100%, 0% 100%);
    margin-top: -50px;
  }

  .footer-section::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background: linear-gradient(180deg, rgba(250, 250, 251, 0.95) 0%, rgba(250, 250, 251, 0.98) 100%);
    z-index: 0;
  }

  .container {
    position: relative;
    z-index: 1;
    max-width: 1440px;
    margin: 0 auto;
  }

  .content {
    display: flex;
    justify-content: space-between;
    gap: 24px;
    margin-bottom: 80px;
  }

  .brand-section {
    flex: 0 0 auto;
    padding-right: 32px;
  }

  .logo-section {
    display: flex;
    flex-direction: column;
    gap: 24px;
  }

  .tagline {
    font-family: 'Shippori Mincho', 'Meiryo UI', 'Hiragino Kaku Gothic ProN', 'Hiragino Sans', sans-serif;
    font-size: 18px;
    font-weight: 400;
    line-height: 1.44;
    color: #61656E;
  }

  .links-section {
    display: flex;
    gap: 100px;
  }

  .links-column {
    display: flex;
    flex-direction: column;
    gap: 32px;
    width: 124px;
  }

  .column-title {
    font-family: 'Shippori Mincho', 'Meiryo UI', 'Hiragino Kaku Gothic ProN', 'Hiragino Sans', sans-serif;
    font-size: 18px;
    font-weight: 500;
    line-height: 1.44;
    color: #12161D;
  }

  .links {
    display: flex;
    flex-direction: column;
    gap: 16px;
  }

  .links a {
    font-family: 'Shippori Mincho', 'Meiryo UI', 'Hiragino Kaku Gothic ProN', 'Hiragino Sans', sans-serif;
    font-size: 16px;
    font-weight: 500;
    color: #61656E;
    text-decoration: none;
    transition: color 0.3s ease;
  }

  .links a:hover {
    color: #12161D;
  }

  .divider {
    width: 100%;
    height: 1px;
    background-color: #E5E5E6;
    margin-bottom: 40px;
  }

  .footer-bottom {
    display: flex;
    justify-content: space-between;
    align-items: center;
    gap: 32px;
  }

  .copyright {
    font-family: 'Shippori Mincho', 'Meiryo UI', 'Hiragino Kaku Gothic ProN', 'Hiragino Sans', sans-serif;
    font-size: 14px;
    font-weight: 400;
    color: #61656E;
  }

  .legal-links {
    display: flex;
    gap: 24px;
    align-items: center;
  }

  .legal-links a {
    font-family: 'Shippori Mincho', 'Meiryo UI', 'Hiragino Kaku Gothic ProN', 'Hiragino Sans', sans-serif;
    font-size: 14px;
    font-weight: 400;
    color: #61656E;
    text-decoration: none;
    transition: color 0.3s ease;
  }

  .legal-links a:hover {
    color: #12161D;
  }

  @media (max-width: 1024px) {
    .content {
      flex-direction: column;
    }

    .links-section {
      flex-wrap: wrap;
      gap: 40px;
    }
  }

  @media (max-width: 768px) {
    .footer-section {
      padding: 60px 20px 20px;
      clip-path: polygon(0 0%, 100% 5%, 100% 100%, 0% 100%);
      margin-top: -30px;
    }

    .content {
      margin-bottom: 60px;
    }

    .brand-section {
      padding-right: 0;
    }

    .links-section {
      flex-direction: column;
      gap: 40px;
    }

    .links-column {
      width: 100%;
    }

    .footer-bottom {
      flex-direction: column;
      align-items: flex-start;
      gap: 20px;
    }

    .legal-links {
      flex-direction: column;
      align-items: flex-start;
      gap: 12px;
    }
  }
</style>
