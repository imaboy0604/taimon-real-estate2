<section class="features3-section">
  <div class="container">
    <div class="content">
      <div class="text-content">
        <h2 class="title">Find Your Dream<br />Home Here</h2>
        <p class="description">
          You can see for yourself how the Perumnas cluster housing offers beautiful and comfortable housing for you and your family. See photos of the house, environment and facilities we provide here.
        </p>
      </div>
      
      <div class="image-content">
        <img 
          src="https://images.unsplash.com/photo-1600585154340-be6161a56a0c?w=1280&h=1111&fit=crop" 
          alt="Dream home showcase"
          class="main-image"
        />
      </div>
    </div>
  </div>
</section>

<style>
  .features3-section {
    background-color: #FFFFFF;
    padding: 120px 80px;
  }

  .container {
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
    font-family: 'Inter Display', sans-serif;
    font-size: 44px;
    font-weight: 500;
    line-height: 1.18;
    color: #12161D;
  }

  .description {
    font-family: 'Inter Display', sans-serif;
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
