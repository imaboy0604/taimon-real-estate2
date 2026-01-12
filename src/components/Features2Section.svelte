<script>
  const features = [
    {
      title: '立地の良さ',
      description: 'タイモン不動産の物件は、各方面からアクセスしやすい立地にあります。都心、空港、駅、バスターミナルなど、重要な場所へ簡単かつ迅速にアクセスできます。'
    },
    {
      title: 'モダンデザイン',
      description: 'タイモン不動産は、モダンで洗練された住まいのデザインを提供しています。お客様の好みやニーズに合わせて、36㎡タイプから120㎡タイプまで、様々なタイプからお選びいただけます。'
    },
    {
      title: 'セキュリティ',
      description: 'タイモン不動産は、統合セキュリティシステムを備えています。各物件にはフェンス、ゲート、警備員が常駐する警備室が設置されており、プロの警備員が監視しています。さらに、各住戸には火災報知器と防犯カメラも完備されています。'
    }
  ];
</script>

<section class="features2-section">
  <div class="container">
    <div class="features-grid">
      {#each features as feature}
        <div class="feature-card">
          <h3 class="feature-title">{feature.title}</h3>
          <p class="feature-description">{feature.description}</p>
        </div>
      {/each}
    </div>
  </div>
</section>

<style>
  .features2-section {
    position: relative;
    background: url('/images/gallery-3.jpg') center/cover;
    padding: 80px 80px 120px 680px;
    overflow: hidden;
    clip-path: polygon(0 0%, 100% 10%, 100% 90%, 0% 100%);
    margin-top: -50px;
  }

  .features2-section::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background: linear-gradient(180deg, rgba(255, 255, 255, 0.88) 0%, rgba(255, 255, 255, 0.82) 100%);
    z-index: 0;
  }

  .container {
    position: relative;
    z-index: 1;
    max-width: 1440px;
    margin: 0 auto;
  }

  .features-grid {
    display: flex;
    flex-direction: column;
    gap: 40px;
  }

  .feature-card {
    display: flex;
    flex-direction: column;
    gap: 24px;
  }

  .feature-title {
    font-family: 'Shippori Mincho', 'Meiryo UI', 'Hiragino Kaku Gothic ProN', 'Hiragino Sans', sans-serif;
    font-size: 24px;
    font-weight: 500;
    line-height: 1.33;
    color: #12161D;
  }

  .feature-description {
    font-family: 'Shippori Mincho', 'Meiryo UI', 'Hiragino Kaku Gothic ProN', 'Hiragino Sans', sans-serif;
    font-size: 18px;
    font-weight: 400;
    line-height: 1.44;
    color: #61656E;
  }

  @media (max-width: 1200px) {
    .features2-section {
      padding: 80px 80px 120px 80px;
    }
  }

  @media (max-width: 768px) {
    .features2-section {
      padding: 60px 20px;
      clip-path: polygon(0 0%, 100% 5%, 100% 95%, 0% 100%);
      margin-top: -30px;
    }

    .features-grid {
      gap: 60px;
    }

    .feature-title {
      font-size: 20px;
    }

    .feature-card {
      gap: 18px;
    }
  }
</style>
