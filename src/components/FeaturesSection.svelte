<script>
</script>

<section class="features-section">
  <div class="container">
    <div class="content">
      <div class="left">
        <h2 class="title">私たちの想い</h2>
      </div>
      
      <div class="right">
        <div class="mission-content">
          <p class="mission-text">
            タイモン不動産は、お客様一人ひとりの「住まいへの想い」を大切にしています。住まいは、人生の基盤となる場所。そこには、家族の笑顔、新しい生活への期待、そして未来への希望が詰まっています。
          </p>
          <p class="mission-text">
            私たちは、単なる物件の紹介だけでなく、お客様の人生のパートナーとして、最適な住まい探しをサポートいたします。お客様のライフスタイル、ご予算、ご希望を丁寧にお伺いし、長く安心してお住まいいただける物件をご提案いたします。
          </p>
          <p class="mission-text">
            住まい探しは、人生の大きな決断の一つです。だからこそ、私たちは誠実に、そして真摯に向き合います。お客様の「理想の住まい」を一緒に見つけていきましょう。
          </p>
        </div>
      </div>
    </div>
  </div>
</section>

<style>
  .features-section {
    position: relative;
    background: url('/images/gallery-1.jpg') center/cover;
    padding: 120px 80px 80px;
    overflow: hidden;
    clip-path: polygon(0 10%, 100% 0%, 100% 90%, 0% 100%);
    margin-top: -50px;
  }

  .features-section::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background: linear-gradient(180deg, rgba(255, 255, 255, 0.85) 0%, rgba(255, 255, 255, 0.75) 100%);
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
    gap: 80px;
    align-items: flex-start;
  }

  .left {
    flex: 0 0 520px;
  }

  .title {
    font-family: 'Shippori Mincho', 'Meiryo UI', 'Hiragino Kaku Gothic ProN', 'Hiragino Sans', sans-serif;
    font-size: 44px;
    font-weight: 500;
    line-height: 1.18;
    color: #12161D;
  }

  .right {
    flex: 1;
    display: flex;
    flex-direction: column;
  }

  .mission-content {
    display: flex;
    flex-direction: column;
    gap: 32px;
  }

  .mission-text {
    font-family: 'Shippori Mincho', 'Meiryo UI', 'Hiragino Kaku Gothic ProN', 'Hiragino Sans', sans-serif;
    font-size: 18px;
    font-weight: 400;
    line-height: 2;
    color: #61656E;
    letter-spacing: 0.05em;
  }

  @media (max-width: 1024px) {
    .content {
      flex-direction: column;
      gap: 60px;
    }

    .left {
      flex: 1;
    }
  }

  @media (max-width: 768px) {
    .features-section {
      padding: 60px 20px;
      clip-path: polygon(0 5%, 100% 0%, 100% 95%, 0% 100%);
      margin-top: -30px;
    }

    .content {
      gap: 32px;
    }

    .title {
      font-size: 36px;
    }

    .mission-content {
      gap: 24px;
    }

    .mission-text {
      font-size: 16px;
      line-height: 1.8;
    }
  }
</style>
