<script lang="ts">
  import ComingSoonModal from './ComingSoonModal.svelte';
  
  export let appName = "Slick Ride";

  let modalOpen = false;
  let modalFeatureName = "";

  function showComingSoon(featureName: string) {
    modalFeatureName = featureName;
    modalOpen = true;
  }
</script>

<nav>
  <div class="container nav-content">
    <div class="logo">
      <span class="logo-text">{appName}</span>
    </div>
    <div class="links">
      <a href="#features">Features</a>
      <button on:click={() => showComingSoon("Ecosystem")}>Ecosystem</button>
      <button on:click={() => showComingSoon("App Download")} class="btn-primary">Get the App</button>
    </div>
  </div>
</nav>

<ComingSoonModal bind:isOpen={modalOpen} featureName={modalFeatureName} />

<style>
  nav {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: var(--header-height);
    display: flex;
    align-items: center;
    background: rgba(3, 3, 5, 0.8);
    backdrop-filter: blur(10px);
    z-index: 100;
    border-bottom: 1px solid rgba(255, 255, 255, 0.05);
  }

  .nav-content {
    display: flex;
    justify-content: space-between;
    align-items: center;
    width: 100%;
  }

  .logo-text {
    font-family: var(--font-heading);
    font-weight: 800;
    font-size: 1.5rem;
    letter-spacing: -0.02em;
    background: linear-gradient(to right, #fff, #aaa);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
  }

  .links {
    display: flex;
    gap: 32px;
    align-items: center;
  }

  .links a,
  .links button {
    font-size: 0.95rem;
    font-weight: 500;
    color: var(--color-text-muted);
    background: none;
    border: none;
    cursor: pointer;
  }

  .links a:hover,
  .links button:hover {
    color: var(--color-text-main);
  }

  .btn-primary {
    background: var(--color-primary);
    color: #000;
    padding: 10px 20px;
    border-radius: 100px;
    font-weight: 700;
    transition: all 0.2s ease;
    box-shadow: 0 0 20px rgba(0, 242, 255, 0.2);
  }

  .btn-primary:hover {
    transform: translateY(-2px);
    box-shadow: 0 0 30px rgba(0, 242, 255, 0.4);
    color: #000;
  }
</style>
