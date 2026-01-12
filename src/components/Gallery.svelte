<script>
  const galleryImages = [
    { id: 1, src: 'https://images.unsplash.com/photo-1560518883-ce09059eeffa?w=560&h=320&fit=crop', alt: 'House exterior' },
    { id: 2, src: 'https://images.unsplash.com/photo-1600585154340-be6161a56a0c?w=600&h=320&fit=crop', alt: 'Modern house' },
    { id: 3, src: 'https://images.unsplash.com/photo-1600607687939-ce8a6c25118c?w=560&h=320&fit=crop', alt: 'House interior' }
  ];
</script>

<section class="gallery-section">
  <div class="container">
    <div class="gallery-grid">
      {#each galleryImages as image}
        <div class="gallery-item">
          <img src={image.src} alt={image.alt} />
        </div>
      {/each}
    </div>
  </div>
</section>

<style>
  .gallery-section {
    background-color: #FFFFFF;
    padding: 40px 80px;
  }

  .container {
    max-width: 1440px;
    margin: 0 auto;
  }

  .gallery-grid {
    display: flex;
    gap: 40px;
    justify-content: center;
  }

  .gallery-item {
    flex: 1;
    max-width: 560px;
    height: 320px;
    overflow: hidden;
    border-radius: 8px;
  }

  .gallery-item img {
    width: 100%;
    height: 100%;
    object-fit: cover;
  }

  @media (max-width: 1024px) {
    .gallery-grid {
      flex-wrap: wrap;
    }

    .gallery-item {
      max-width: 100%;
    }
  }

  @media (max-width: 768px) {
    .gallery-section {
      padding: 60px 16px;
    }

    .gallery-grid {
      flex-direction: column;
      gap: 24px;
    }

    .gallery-item {
      height: 230px;
    }
  }
</style>
