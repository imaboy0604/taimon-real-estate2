<section class="features3-section">
  <div class="container">
    <div class="content">
      <div class="text-content">
        <h2 class="title">理想の住まいを<br />ここで見つける</h2>
        <p class="description">
          タイモン不動産が、あなたとご家族のために美しく快適な住まいを提供する様子を、ぜひご覧ください。物件、環境、そして私たちが提供する施設の写真をご覧いただけます。
        </p>
      </div>
      
      <div class="image-content">
        <img 
          src="/images/dream-home.jpg" 
          alt="理想の住まい"
          class="main-image"
        />
      </div>
    </div>
  </div>
</section>

<style>
  .features3-section {
    position: relative;
    background: url('/images/gallery-1.jpg') center/cover;
    padding: 120px 80px;
    overflow: hidden;
    clip-path: polygon(0 0%, 100% 10%, 100% 90%, 0% 100%);
    margin-top: -50px;
  }

  .features3-section::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background: linear-gradient(180deg, rgba(255, 255, 255, 0.9) 0%, rgba(255, 255, 255, 0.85) 100%);
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
    flex-direction: column;
    gap: 80px;
  }

  .text-content {
    display: flex;
    flex-direction: column;
    gap: 24px;
    max-width: 550px;
  }

  .title {
    font-family: 'Shippori Mincho', 'Meiryo UI', 'Hiragino Kaku Gothic ProN', 'Hiragino Sans', sans-serif;
    font-size: 44px;
    font-weight: 500;
    line-height: 1.18;
    color: #12161D;
  }

  .description {
    font-family: 'Shippori Mincho', 'Meiryo UI', 'Hiragino Kaku Gothic ProN', 'Hiragino Sans', sans-serif;
    font-size: 18px;
    font-weight: 400;
    line-height: 1.44;
    color: #61656E;
    max-width: 550px;
  }

  .image-content {
    width: 100%;
  }

  .main-image {
    width: 100%;
    max-width: 1280px;
    height: auto;
    border-radius: 8px;
    object-fit: cover;
  }

  @media (max-width: 768px) {
    .features3-section {
      padding: 60px 20px;
      clip-path: polygon(0 0%, 100% 5%, 100% 95%, 0% 100%);
      margin-top: -30px;
    }

    .content {
      gap: 60px;
    }

    .title {
      font-size: 36px;
    }

    .text-content {
      max-width: 100%;
    }

    .description {
      max-width: 100%;
    }
  }
</style>
