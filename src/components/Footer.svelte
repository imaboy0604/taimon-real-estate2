<section class="footer-section">
  <div class="container">
    <div class="content">
      <div class="brand-section">
        <div class="logo-section">
          <div class="logo">
            <svg width="137" height="32" viewBox="0 0 137 32" fill="none" xmlns="http://www.w3.org/2000/svg">
              <text x="0" y="22" font-family="Inter Display" font-size="24" font-weight="500" fill="#12161D">タイモン不動産</text>
            </svg>
          </div>
          <p class="tagline">
            More Comfortable.<br />
            More Classy.
          </p>
        </div>
      </div>

      <div class="links-section">
        <div class="links-column">
          <h3 class="column-title">Product</h3>
          <div class="links">
            <a href="#features">Features</a>
            <a href="#integrations">Integrations</a>
            <a href="#pricing">Pricing</a>
          </div>
        </div>

        <div class="links-column">
          <h3 class="column-title">Company</h3>
          <div class="links">
            <a href="#about">About us</a>
            <a href="#blog">Blog</a>
            <a href="#careers">Careers</a>
            <a href="#customers">Customers</a>
            <a href="#brand">Brand</a>
          </div>
        </div>

        <div class="links-column">
          <h3 class="column-title">Resources</h3>
          <div class="links">
            <a href="#community">Community</a>
            <a href="#contact">Contact</a>
            <a href="#dpa">DPA</a>
            <a href="#terms">Terms of service</a>
          </div>
        </div>
      </div>
    </div>

    <div class="divider"></div>

    <div class="footer-bottom">
      <p class="copyright">© 2022 Perumnas. All rights reserved</p>
      <div class="legal-links">
        <a href="#terms">Terms of Service</a>
        <a href="#policy">Policy service</a>
        <a href="#cookie">Cookie Policy</a>
        <a href="#partners">Partners</a>
      </div>
    </div>
  </div>
</section>

<style>
  .footer-section {
    background-color: #FAFAFB;
    padding: 80px 80px 40px;
  }

  .container {
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
    font-family: 'Inter Display', sans-serif;
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
    font-family: 'Inter Display', sans-serif;
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
    font-family: 'Inter Display', sans-serif;
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
    font-family: 'Inter Display', sans-serif;
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
    font-family: 'Inter Display', sans-serif;
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
