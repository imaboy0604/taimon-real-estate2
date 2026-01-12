<script>
  import HeroSection from './components/HeroSection.svelte';
  import FeaturesSection from './components/FeaturesSection.svelte';
  import Gallery from './components/Gallery.svelte';
  import Features2Section from './components/Features2Section.svelte';
  import Features3Section from './components/Features3Section.svelte';
  import FAQSection from './components/FAQSection.svelte';
  import Footer from './components/Footer.svelte';
</script>

<main>
  <HeroSection />
  <FeaturesSection />
  <Gallery />
  <Features2Section />
  <Features3Section />
  <FAQSection />
  <Footer />
</main>

<style>
  :global(*) {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }

  :global(html) {
    scroll-behavior: smooth;
  }

  :global(body) {
    font-family: 'Inter Display', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
    color: #12161D;
    background-color: #FFFFFF;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
  }

  main {
    width: 100%;
    overflow-x: hidden;
  }
</style>
