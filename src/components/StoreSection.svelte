<script>
  import { onMount } from 'svelte';
  
  const storeImages = [
    { id: 1, src: '/images/store-exterior.jpg', alt: '店舗外観', label: '外観' },
    { id: 2, src: '/images/store-interior-1.jpg', alt: '店舗内観1', label: '内観' },
    { id: 3, src: '/images/store-interior-2.jpg', alt: '店舗内観2', label: '内観' },
  ];
  
  let currentIndex = 0;
  let intervalId;
  
  function nextImage() {
    currentIndex = (currentIndex + 1) % storeImages.length;
  }
  
  function prevImage() {
    currentIndex = (currentIndex - 1 + storeImages.length) % storeImages.length;
  }
  
  function goToImage(index) {
    currentIndex = index;
  }
  
  onMount(() => {
    // 5秒ごとに自動切り替え
    intervalId = setInterval(nextImage, 5000);
    return () => {
      if (intervalId) clearInterval(intervalId);
    };
  });
</script>

<section class="store-section">
  <div class="container">
    <div class="header">
      <h2 class="title">店舗紹介</h2>
      <p class="subtitle">
        タイモン不動産の店舗をご紹介します。<br />
        お気軽にご来店ください。
      </p>
    </div>

    <div class="store-carousel">
      <div class="carousel-container">
        <button class="carousel-button prev" on:click={prevImage} aria-label="前の画像">
          <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path d="M15 18L9 12L15 6" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
          </svg>
        </button>
        
        <div class="carousel-slide">
          {#each storeImages as image, index}
            <div class="slide-item" class:active={index === currentIndex}>
              <div class="image-wrapper">
                <img src={image.src} alt={image.alt} />
                <div class="image-label">{image.label}</div>
              </div>
            </div>
          {/each}
        </div>
        
        <button class="carousel-button next" on:click={nextImage} aria-label="次の画像">
          <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path d="M9 18L15 12L9 6" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
          </svg>
        </button>
      </div>
      
      <div class="carousel-indicators">
        {#each storeImages as image, index}
          <button 
            class="indicator" 
            class:active={index === currentIndex}
            on:click={() => goToImage(index)}
            aria-label="画像{index + 1}に移動"
          ></button>
        {/each}
      </div>
    </div>

    <div class="store-info">
      <div class="info-item">
        <h3 class="info-title">営業時間</h3>
        <p class="info-text">平日：10:00 - 19:00<br />土日祝：10:00 - 18:00</p>
      </div>
      <div class="info-item">
        <h3 class="info-title">アクセス</h3>
        <p class="info-text">JR各線「○○駅」徒歩5分<br />駐車場完備（5台）</p>
      </div>
      <div class="info-item">
        <h3 class="info-title">お問い合わせ</h3>
        <p class="info-text">TEL: 03-XXXX-XXXX<br />MAIL: info@taimon-real-estate.jp</p>
      </div>
    </div>
  </div>
</section>

<style>
  .store-section {
    position: relative;
    background: url('/images/gallery-2.jpg') center/cover;
    padding: 120px 80px;
    overflow: hidden;
    clip-path: polygon(0 0%, 100% 10%, 100% 90%, 0% 100%);
    margin-top: -50px;
  }

  .store-section::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background: linear-gradient(180deg, rgba(255, 255, 255, 0.92) 0%, rgba(255, 255, 255, 0.88) 100%);
    z-index: 0;
  }

  .container {
    position: relative;
    z-index: 1;
    max-width: 1440px;
    margin: 0 auto;
  }

  .header {
    text-align: center;
    margin-bottom: 80px;
  }

  .title {
    font-family: 'Shippori Mincho', 'Meiryo UI', 'Hiragino Kaku Gothic ProN', 'Hiragino Sans', sans-serif;
    font-size: 44px;
    font-weight: 500;
    line-height: 1.18;
    color: #12161D;
    margin-bottom: 24px;
  }

  .subtitle {
    font-family: 'Shippori Mincho', 'Meiryo UI', 'Hiragino Kaku Gothic ProN', 'Hiragino Sans', sans-serif;
    font-size: 18px;
    font-weight: 400;
    line-height: 1.44;
    color: #61656E;
  }

  .store-carousel {
    margin-bottom: 80px;
  }

  .carousel-container {
    position: relative;
    max-width: 600px;
    margin: 0 auto;
    display: flex;
    align-items: center;
    gap: 16px;
  }

  .carousel-button {
    background: rgba(255, 255, 255, 0.9);
    border: none;
    border-radius: 50%;
    width: 48px;
    height: 48px;
    display: flex;
    align-items: center;
    justify-content: center;
    cursor: pointer;
    transition: all 0.3s ease;
    color: #12161D;
    box-shadow: 0 4px 12px rgba(0, 0, 0, 0.15);
    z-index: 10;
    flex-shrink: 0;
  }

  .carousel-button:hover {
    background: white;
    transform: scale(1.1);
    box-shadow: 0 6px 16px rgba(0, 0, 0, 0.2);
  }

  .carousel-button:active {
    transform: scale(0.95);
  }

  .carousel-slide {
    position: relative;
    width: 100%;
    height: 400px;
    overflow: hidden;
    border-radius: 16px;
    box-shadow: 0 8px 24px rgba(0, 0, 0, 0.15);
  }

  .slide-item {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    opacity: 0;
    transition: opacity 0.5s ease-in-out;
  }

  .slide-item.active {
    opacity: 1;
    z-index: 1;
  }

  .image-wrapper {
    position: relative;
    width: 100%;
    height: 100%;
    overflow: hidden;
  }

  .image-wrapper img {
    width: 100%;
    height: 100%;
    object-fit: cover;
  }

  .image-label {
    position: absolute;
    bottom: 16px;
    left: 16px;
    background: rgba(0, 0, 0, 0.7);
    color: white;
    padding: 8px 16px;
    border-radius: 20px;
    font-family: 'Shippori Mincho', 'Meiryo UI', 'Hiragino Kaku Gothic ProN', 'Hiragino Sans', sans-serif;
    font-size: 14px;
    font-weight: 500;
    z-index: 2;
  }

  .carousel-indicators {
    display: flex;
    justify-content: center;
    gap: 12px;
    margin-top: 24px;
  }

  .indicator {
    width: 12px;
    height: 12px;
    border-radius: 50%;
    border: 2px solid #12161D;
    background: transparent;
    cursor: pointer;
    transition: all 0.3s ease;
    padding: 0;
  }

  .indicator.active {
    background: #12161D;
    transform: scale(1.2);
  }

  .indicator:hover {
    transform: scale(1.1);
  }

  .store-info {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 60px;
    padding-top: 60px;
    border-top: 1px solid #E5E5E6;
  }

  .info-item {
    text-align: center;
  }

  .info-title {
    font-family: 'Shippori Mincho', 'Meiryo UI', 'Hiragino Kaku Gothic ProN', 'Hiragino Sans', sans-serif;
    font-size: 24px;
    font-weight: 500;
    line-height: 1.33;
    color: #12161D;
    margin-bottom: 16px;
  }

  .info-text {
    font-family: 'Shippori Mincho', 'Meiryo UI', 'Hiragino Kaku Gothic ProN', 'Hiragino Sans', sans-serif;
    font-size: 16px;
    font-weight: 400;
    line-height: 1.8;
    color: #61656E;
  }

  @media (max-width: 1024px) {
    .carousel-container {
      max-width: 500px;
    }

    .carousel-slide {
      height: 350px;
    }

    .store-info {
      grid-template-columns: 1fr;
      gap: 40px;
    }
  }

  @media (max-width: 768px) {
    .store-section {
      padding: 80px 20px;
      clip-path: polygon(0 0%, 100% 5%, 100% 95%, 0% 100%);
      margin-top: -30px;
    }

    .header {
      margin-bottom: 60px;
    }

    .title {
      font-size: 36px;
    }

    .carousel-container {
      max-width: 100%;
      gap: 8px;
    }

    .carousel-button {
      width: 40px;
      height: 40px;
    }

    .carousel-slide {
      height: 300px;
    }

    .store-info {
      gap: 32px;
      padding-top: 40px;
    }
  }
</style>
