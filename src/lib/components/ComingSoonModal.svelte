<script lang="ts">
  export let isOpen = false;
  export let featureName = "This feature";

  function closeModal() {
    isOpen = false;
  }

  function handleBackdropClick(e: MouseEvent) {
    if (e.target === e.currentTarget) {
      closeModal();
    }
  }
</script>

{#if isOpen}
  <div class="modal-backdrop" on:click={handleBackdropClick} role="presentation">
    <div class="modal">
      <button class="close-btn" on:click={closeModal} aria-label="Close modal">
        &times;
      </button>
      <div class="modal-content">
        <div class="icon">🚀</div>
        <h2>Coming Soon!</h2>
        <p>{featureName} is currently under development.</p>
        <p class="sub-text">We're working hard to bring you the best experience. Stay tuned!</p>
        <button class="btn-ok" on:click={closeModal}>Got it!</button>
      </div>
    </div>
  </div>
{/if}

<style>
  .modal-backdrop {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: rgba(0, 0, 0, 0.8);
    backdrop-filter: blur(5px);
    display: flex;
    align-items: center;
    justify-content: center;
    z-index: 1000;
    animation: fadeIn 0.2s ease;
  }

  @keyframes fadeIn {
    from {
      opacity: 0;
    }
    to {
      opacity: 1;
    }
  }

  .modal {
    background: linear-gradient(135deg, rgba(20, 20, 25, 0.98), rgba(10, 10, 15, 0.98));
    border: 1px solid rgba(0, 242, 255, 0.3);
    border-radius: 20px;
    padding: 40px;
    max-width: 450px;
    width: 90%;
    position: relative;
    box-shadow: 0 20px 60px rgba(0, 242, 255, 0.2);
    animation: slideUp 0.3s ease;
  }

  @keyframes slideUp {
    from {
      transform: translateY(20px);
      opacity: 0;
    }
    to {
      transform: translateY(0);
      opacity: 1;
    }
  }

  .close-btn {
    position: absolute;
    top: 16px;
    right: 16px;
    background: none;
    border: none;
    font-size: 2rem;
    color: rgba(255, 255, 255, 0.5);
    cursor: pointer;
    line-height: 1;
    padding: 4px 8px;
    transition: color 0.2s ease;
  }

  .close-btn:hover {
    color: var(--color-primary);
  }

  .modal-content {
    text-align: center;
  }

  .icon {
    font-size: 4rem;
    margin-bottom: 16px;
    animation: bounce 0.6s ease;
  }

  @keyframes bounce {
    0%, 100% {
      transform: translateY(0);
    }
    50% {
      transform: translateY(-10px);
    }
  }

  h2 {
    font-size: 2rem;
    font-weight: 800;
    margin-bottom: 16px;
    background: linear-gradient(to right, var(--color-primary), #fff);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
  }

  p {
    color: var(--color-text-muted);
    margin-bottom: 12px;
    font-size: 1rem;
    line-height: 1.6;
  }

  .sub-text {
    font-size: 0.9rem;
    margin-bottom: 24px;
  }

  .btn-ok {
    background: var(--color-primary);
    color: #000;
    padding: 12px 32px;
    border-radius: 100px;
    font-weight: 700;
    font-size: 1rem;
    border: none;
    cursor: pointer;
    transition: all 0.2s ease;
    box-shadow: 0 0 20px rgba(0, 242, 255, 0.3);
  }

  .btn-ok:hover {
    transform: translateY(-2px);
    box-shadow: 0 0 30px rgba(0, 242, 255, 0.5);
  }

  @media (max-width: 768px) {
    .modal {
      padding: 30px 20px;
    }

    h2 {
      font-size: 1.5rem;
    }

    .icon {
      font-size: 3rem;
    }
  }
</style>
