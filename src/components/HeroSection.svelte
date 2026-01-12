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
        <svg width="20" height="20" viewBox="0 0 20 20" fill="none" xmlns="http://www.w3.org/2000/svg">
          <path d="M2.5 5H17.5M2.5 10H17.5M2.5 15H17.5" stroke="currentColor" stroke-width="1.5" stroke-linecap="round"/>
        </svg>
        <span>Menu</span>
      </button>
      
      <div class="logo">
        <svg width="120" height="28" viewBox="0 0 120 28" fill="none" xmlns="http://www.w3.org/2000/svg">
          <text x="0" y="20" font-family="Inter Display" font-size="24" font-weight="500" fill="white">タイモン不動産</text>
        </svg>
      </div>
      
      <div class="nav-links">
        <a href="#contact">Contact Us</a>
        <a href="#about">About Us</a>
      </div>
    </div>
  </nav>

  <div class="hero-content">
    <h1 class="hero-title">
      More Comfortable.<br />
      More Classy.
    </h1>
    <p class="hero-subtitle">
      Make your living experience even more memorable.
    </p>
  </div>
</section>

<style>
  .hero-section {
    position: relative;
    width: 100%;
    height: 512px;
    background: linear-gradient(180deg, rgba(83, 131, 169, 1) 0%, rgba(83, 131, 169, 0.39) 55%, rgba(92, 138, 176, 0) 100%),
                url('https://images.unsplash.com/photo-1560518883-ce09059eeffa?w=1440&h=512&fit=crop') center/cover;
    display: flex;
    flex-direction: column;
    color: white;
  }

  .overlay-top {
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    height: 512px;
    background: linear-gradient(180deg, rgba(83, 131, 169, 1) 0%, rgba(83, 131, 169, 0.39) 55%, rgba(92, 138, 176, 0) 100%);
  }

  .overlay-bottom {
    position: absolute;
    bottom: 0;
    left: 0;
    right: 0;
    height: 240px;
    background: linear-gradient(180deg, rgba(255, 255, 255, 0) 0%, rgba(255, 255, 255, 0.37) 20%, rgba(255, 255, 255, 0.78) 39%, rgba(255, 255, 255, 0.94) 65%, rgba(255, 255, 255, 1) 89%);
  }

  .navbar {
    position: relative;
    z-index: 10;
    padding: 20px 40px;
  }

  .navbar-content {
    display: flex;
    justify-content: space-between;
    align-items: center;
    max-width: 1440px;
    margin: 0 auto;
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
    font-family: 'Inter Display', sans-serif;
    font-size: 16px;
    font-weight: 500;
    color: #12161D;
  }

  .logo {
    flex: 1;
    display: flex;
    justify-content: center;
  }

  .nav-links {
    display: flex;
    gap: 24px;
  }

  .nav-links a {
    font-family: 'Inter Display', sans-serif;
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
    padding: 80px 0;
    text-align: center;
  }

  .hero-title {
    font-family: 'Inter Display', sans-serif;
    font-size: 72px;
    font-weight: 500;
    line-height: 1.11;
    letter-spacing: -0.025em;
    max-width: 624px;
  }

  .hero-subtitle {
    font-family: 'Inter Display', sans-serif;
    font-size: 18px;
    font-weight: 400;
    line-height: 1.44;
    opacity: 1;
  }

  @media (max-width: 768px) {
    .hero-section {
      height: 435px;
    }

    .navbar {
      padding: 12px 16px;
    }

    .navbar-content {
      gap: 0;
    }

    .menu-button {
      padding: 8px 14px;
      font-size: 14px;
    }

    .nav-links {
      display: none;
    }

    .hero-title {
      font-size: 44px;
      padding: 0 15px;
    }

    .hero-subtitle {
      font-size: 18px;
      padding: 0 15px;
    }

    .hero-content {
      padding: 60px 0;
      gap: 14px;
    }
  }
</style>
