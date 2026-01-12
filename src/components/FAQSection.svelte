<script>
  let openIndex = 0;

  const faqs = [
    {
      question: 'What is cluster housing perumnas?',
      answer: 'Cluster housing perumnas is a housing concept that consists of several houses in a gated cluster. Cluster housing perumnas offers comfortable, secure, and affordable housing with various complete and modern facilities.'
    },
    {
      question: 'Where is the location of cluster housing perumnas?',
      answer: 'Cluster housing perumnas is strategically located in easily accessible areas with good connectivity to city centers, airports, and other important facilities.'
    },
    {
      question: 'How much are the prices and types of houses in cluster housing perumnas?',
      answer: 'Cluster housing perumnas offers various house types ranging from type 36 to type 120. Prices vary depending on the type and location. Please contact us for detailed pricing information.'
    },
    {
      question: 'What are the facilities provided in cluster housing perumnas?',
      answer: 'Cluster housing perumnas provides various facilities including playgrounds, sports fields, shopping centers, schools, security systems, and other modern amenities.'
    }
  ];

  function toggleFAQ(index) {
    openIndex = openIndex === index ? -1 : index;
  }
</script>

<section class="faq-section">
  <div class="container">
    <div class="content">
      <div class="header">
        <h2 class="title">Frequently Asked Questions</h2>
        <p class="subtitle">
          If there are question you want to ask.<br />
          We will answer all your question.
        </p>
      </div>

      <div class="faq-list">
        {#each faqs as faq, index}
          <div class="faq-item" class:open={openIndex === index}>
            <button class="faq-question" on:click={() => toggleFAQ(index)}>
              <span>{faq.question}</span>
              <svg 
                width="24" 
                height="24" 
                viewBox="0 0 24 24" 
                fill="none" 
                xmlns="http://www.w3.org/2000/svg"
                class="icon"
              >
                {#if openIndex === index}
                  <path d="M5 12H19" stroke="currentColor" stroke-width="2" stroke-linecap="round"/>
                {:else}
                  <path d="M12 5V19M5 12H19" stroke="currentColor" stroke-width="2" stroke-linecap="round"/>
                {/if}
              </svg>
            </button>
            {#if openIndex === index}
              <div class="faq-answer">
                <p>{faq.answer}</p>
              </div>
            {/if}
          </div>
        {/each}
      </div>
    </div>
  </div>
</section>

<style>
  .faq-section {
    background-color: #FFFFFF;
    padding: 120px 80px;
  }

  .container {
    max-width: 1440px;
    margin: 0 auto;
  }

  .content {
    display: flex;
    justify-content: center;
    gap: 64px;
  }

  .header {
    display: flex;
    flex-direction: column;
    gap: 24px;
    flex: 0 0 auto;
  }

  .title {
    font-family: 'Inter Display', sans-serif;
    font-size: 44px;
    font-weight: 500;
    line-height: 1.18;
    color: #12161D;
  }

  .subtitle {
    font-family: 'Inter Display', sans-serif;
    font-size: 18px;
    font-weight: 400;
    line-height: 1.44;
    color: #61656E;
  }

  .faq-list {
    flex: 1;
    display: flex;
    flex-direction: column;
    gap: 20px;
    max-width: 600px;
  }

  .faq-item {
    border: 1px solid #E5E5E6;
    border-radius: 8px;
    background-color: #FFFFFF;
    overflow: hidden;
    transition: all 0.3s ease;
  }

  .faq-item.open {
    border-color: #12161D;
  }

  .faq-question {
    width: 100%;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 24px;
    background: none;
    border: none;
    text-align: left;
    cursor: pointer;
    font-family: 'Inter Display', sans-serif;
    font-size: 24px;
    font-weight: 500;
    line-height: 1.33;
    color: #12161D;
  }

  .faq-question .icon {
    flex-shrink: 0;
    color: #12161D;
  }

  .faq-answer {
    padding: 0 24px 24px 24px;
  }

  .faq-answer p {
    font-family: 'Inter Display', sans-serif;
    font-size: 18px;
    font-weight: 400;
    line-height: 1.44;
    color: #61656E;
  }

  @media (max-width: 1024px) {
    .content {
      flex-direction: column;
      gap: 40px;
    }

    .header {
      text-align: center;
    }
  }

  @media (max-width: 768px) {
    .faq-section {
      padding: 60px 20px;
    }

    .content {
      gap: 60px;
    }

    .title {
      font-size: 36px;
    }

    .faq-question {
      font-size: 20px;
      padding: 20px;
    }

    .faq-answer {
      padding: 0 20px 20px 20px;
    }
  }
</style>
