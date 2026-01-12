<script>
  // カルーセルの現在のページ（例：5ページ中1ページ目）
  let currentPage = 1;
  const totalPages = 5;
  
  // スクロール時のヘッダー背景変更
  let scrolled = false;
  
  function handleScroll() {
    scrolled = window.scrollY > 50;
  }
  
  import { onMount, onDestroy } from 'svelte';
  
  onMount(() => {
    window.addEventListener('scroll', handleScroll);
    return () => {
      window.removeEventListener('scroll', handleScroll);
    };
  });
</script>

<header class="header" class:scrolled={scrolled}>
  <div class="header-content">
    <div class="header-left">
      <!-- 左側は空（必要に応じてロゴなどを配置可能） -->
    </div>
    
    <div class="header-center">
      <!-- パジネーションドット（カルーセル用） -->
      <div class="pagination-dots">
        {#each Array(totalPages) as _, index}
          <button
            class="dot"
            class:active={index + 1 === currentPage}
            on:click={() => currentPage = index + 1}
            aria-label="ページ{index + 1}に移動"
          ></button>
        {/each}
      </div>
    </div>
    
    <div class="header-right">
      <!-- 右側は空（必要に応じてテキストなどを配置可能） -->
    </div>
  </div>
</header>

<style>
  .header {
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    z-index: 1000;
    /* 写真がくっきり見えるように完全に透明な背景 */
    background-color: transparent;
    backdrop-filter: none;
    transition: all var(--transition-base, 0.3s ease);
    padding: var(--spacing-2, 16px) 0;
  }
  
  /* スクロール時に少し背景を追加（オプション） */
  .header.scrolled {
    background-color: rgba(255, 255, 255, 0.95);
    backdrop-filter: blur(10px);
    box-shadow: var(--shadow-subtle, 0 2px 8px rgba(0, 0, 0, 0.08));
  }
  
  .header-content {
    display: grid;
    grid-template-columns: 1fr auto 1fr;
    align-items: center;
    max-width: var(--breakpoint-desktop, 1440px);
    margin: 0 auto;
    padding: 0 var(--padding-container, 32px);
    width: 100%;
  }
  
  .header-left,
  .header-right {
    display: flex;
    align-items: center;
  }
  
  .header-left {
    justify-content: flex-start;
  }
  
  .header-right {
    justify-content: flex-end;
  }
  
  .header-center {
    display: flex;
    justify-content: center;
    align-items: center;
  }
  
  .pagination-dots {
    display: flex;
    gap: var(--spacing-1, 8px);
    align-items: center;
  }
  
  .dot {
    width: 8px;
    height: 8px;
    border-radius: 50%;
    border: none;
    background-color: rgba(255, 255, 255, 0.6);
    cursor: pointer;
    transition: all var(--transition-base, 0.3s ease);
    padding: 0;
    outline: none;
  }
  
  .dot:hover {
    background-color: rgba(255, 255, 255, 0.9);
    transform: scale(1.2);
  }
  
  .dot.active {
    background-color: rgba(255, 255, 255, 1);
    width: 10px;
    height: 10px;
    box-shadow: 0 0 4px rgba(255, 255, 255, 0.5);
  }
  
  .header.scrolled .dot {
    background-color: rgba(0, 0, 0, 0.2);
  }
  
  .header.scrolled .dot:hover {
    background-color: rgba(0, 0, 0, 0.3);
  }
  
  .header.scrolled .dot.active {
    background-color: var(--color-text-primary, #1A1A1A);
  }
  
  /* モバイル対応 */
  @media (max-width: 768px) {
    .header {
      padding: var(--spacing-1, 8px) 0;
    }
    
    .header-content {
      padding: 0 var(--spacing-2, 16px);
    }
    
    .dot {
      width: 6px;
      height: 6px;
    }
    
    .dot.active {
      width: 8px;
      height: 8px;
    }
  }
</style>
