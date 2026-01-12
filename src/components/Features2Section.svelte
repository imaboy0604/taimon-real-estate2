<script>
  const features = [
    {
      title: 'Strategic Location',
      description: 'Cluster housing perumnas is located in an area that is easily accessible from various directions. You can reach the city center, airport, train station, bus terminal, and other important places easily and quickly.'
    },
    {
      title: 'Modern Design',
      description: 'Cluster housing perumnas has a modern and elegant house design. You can choose the type of house that suits your taste and needs, ranging from type 36 to type 120.'
    },
    {
      title: 'Guaranteed Security',
      description: 'Cluster housing perumnas has an integrated security system. Each cluster is equipped with a fence, gate, and guard post that are monitored by professional security officers. In addition, each house is also equipped with a fire alarm and CCTV.'
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
    background-color: #FFFFFF;
    padding: 80px 80px 120px 680px;
  }

  .container {
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
    font-family: 'Inter Display', sans-serif;
    font-size: 24px;
    font-weight: 500;
    line-height: 1.33;
    color: #12161D;
  }

  .feature-description {
    font-family: 'Inter Display', sans-serif;
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
