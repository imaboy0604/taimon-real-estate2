<script>
  let openIndex = 0;

  const faqs = [
    {
      question: 'タイモン不動産とは何ですか？',
      answer: 'タイモン不動産は、ゲート付きの物件群で構成される住まいのコンセプトです。快適で安全、そして手頃な価格の住まいを、様々な充実したモダンな施設と共に提供しています。'
    },
    {
      question: 'タイモン不動産の物件はどこにありますか？',
      answer: 'タイモン不動産の物件は、都心、空港、その他の重要な施設へのアクセスが容易な、戦略的に選ばれた立地にあります。'
    },
    {
      question: 'タイモン不動産の物件の価格とタイプはどのくらいですか？',
      answer: 'タイモン不動産は、36㎡タイプから120㎡タイプまで、様々なタイプの物件を提供しています。価格はタイプと立地によって異なります。詳細な価格情報については、お気軽にお問い合わせください。'
    },
    {
      question: 'タイモン不動産ではどのような施設が提供されていますか？',
      answer: 'タイモン不動産では、遊び場、スポーツ施設、ショッピングセンター、学校、セキュリティシステムなど、様々なモダンな施設を提供しています。'
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
        <h2 class="title">よくある質問</h2>
        <p class="subtitle">
          ご質問がございましたら、<br />
          お気軽にお問い合わせください。
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
    position: relative;
    background: url('/images/gallery-2.jpg') center/cover;
    padding: 120px 80px;
    overflow: hidden;
    clip-path: polygon(0 0%, 100% 10%, 100% 100%, 0% 90%);
    margin-top: -50px;
  }

  .faq-section::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background: linear-gradient(180deg, rgba(255, 255, 255, 0.92) 0%, rgba(255, 255, 255, 0.88) 100%);
    z-index: 0;
  }

  .container {
    position: relative;
    z-index: 1;
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
    font-family: 'Shippori Mincho', 'Meiryo UI', 'Hiragino Kaku Gothic ProN', 'Hiragino Sans', sans-serif;
    font-size: 44px;
    font-weight: 500;
    line-height: 1.18;
    color: #12161D;
  }

  .subtitle {
    font-family: 'Shippori Mincho', 'Meiryo UI', 'Hiragino Kaku Gothic ProN', 'Hiragino Sans', sans-serif;
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
    font-family: 'Shippori Mincho', 'Meiryo UI', 'Hiragino Kaku Gothic ProN', 'Hiragino Sans', sans-serif;
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
    font-family: 'Shippori Mincho', 'Meiryo UI', 'Hiragino Kaku Gothic ProN', 'Hiragino Sans', sans-serif;
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
      clip-path: polygon(0 0%, 100% 5%, 100% 100%, 0% 95%);
      margin-top: -30px;
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
