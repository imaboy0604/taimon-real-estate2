<script>
  const features = [
    { value: '+100', label: 'Units Ready' },
    { value: '+60K', label: 'Customers' },
    { value: '+70K', label: 'Review' }
  ];
</script>

<section class="features-section">
  <div class="container">
    <div class="content">
      <div class="left">
        <h2 class="title">Enjoy Quality Life in Perumnas Housing</h2>
      </div>
      
      <div class="right">
        <p class="description">
          Perumnas cluster housing is the right choice for those of you who are looking for comfortable, safe and affordable housing. With the cluster concept, you can enjoy the privacy and comfort of living in a beautiful and clean environment. Apart from that, you can also enjoy the various facilities provided, such as playgrounds, sports fields, shopping centers, schools, and others.
        </p>
        
        <div class="key-features">
          {#each features as feature}
            <div class="feature-item">
              <div class="feature-value">{feature.value}</div>
              <div class="feature-label">{feature.label}</div>
            </div>
          {/each}
        </div>
      </div>
    </div>
  </div>
</section>

<style>
  .features-section {
    background-color: #FFFFFF;
    padding: 120px 80px 80px;
  }

  .container {
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
    font-family: 'Inter Display', sans-serif;
    font-size: 44px;
    font-weight: 500;
    line-height: 1.18;
    color: #12161D;
  }

  .right {
    flex: 1;
    display: flex;
    flex-direction: column;
    gap: 80px;
  }

  .description {
    font-family: 'Inter Display', sans-serif;
    font-size: 18px;
    font-weight: 400;
    line-height: 1.44;
    color: #61656E;
  }

  .key-features {
    display: flex;
    gap: 80px;
    align-items: stretch;
  }

  .feature-item {
    flex: 1;
    display: flex;
    flex-direction: column;
    gap: 12px;
  }

  .feature-value {
    font-family: 'Inter Display', sans-serif;
    font-size: 36px;
    font-weight: 500;
    line-height: 1.33;
    color: #12161D;
  }

  .feature-label {
    font-family: 'Inter Display', sans-serif;
    font-size: 18px;
    font-weight: 400;
    line-height: 1.44;
    color: #61656E;
  }

  @media (max-width: 1024px) {
    .content {
      flex-direction: column;
      gap: 60px;
    }

    .left {
      flex: 1;
    }

    .key-features {
      gap: 40px;
    }
  }

  @media (max-width: 768px) {
    .features-section {
      padding: 60px 20px;
    }

    .content {
      gap: 32px;
    }

    .title {
      font-size: 36px;
    }

    .right {
      gap: 60px;
    }

    .key-features {
      flex-direction: column;
      gap: 40px;
    }

    .feature-item {
      align-items: center;
      text-align: center;
    }

    .feature-value {
      font-size: 24px;
    }
  }
</style>
