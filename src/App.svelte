<script>
  import HeroSection from './components/HeroSection.svelte';
  import FeaturesSection from './components/FeaturesSection.svelte';
  import StoreSection from './components/StoreSection.svelte';
  import Features2Section from './components/Features2Section.svelte';
  import Features3Section from './components/Features3Section.svelte';
  import FAQSection from './components/FAQSection.svelte';
  import Footer from './components/Footer.svelte';
</script>

<main>
  <HeroSection />
  <FeaturesSection />
  <StoreSection />
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
    margin: 0;
    padding: 0;
    width: 100%;
    overflow-x: hidden;
  }

  :global(body) {
    font-family: 'Shippori Mincho', 'Meiryo UI', 'Hiragino Kaku Gothic ProN', 'Hiragino Sans', 'Noto Sans JP', sans-serif;
    color: #12161D;
    background-color: #FFFFFF;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    margin: 0;
    padding: 0;
    width: 100%;
    overflow-x: hidden;
  }

  main {
    width: 100%;
    margin: 0;
    padding: 0;
    overflow-x: hidden;
  }
</style>
