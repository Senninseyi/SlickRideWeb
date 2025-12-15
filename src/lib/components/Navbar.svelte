<script lang="ts">
  export let appName = "Slick Ride";
</script>

<nav>
  <div class="container nav-content">
    <div class="logo">
      <span class="logo-text">{appName}</span>
    </div>
    <div class="links">
      <a href="#features">Features</a>
      <a href="#ecosystem">Ecosystem</a>
      <a href="#download" class="btn-primary">Get the App</a>
    </div>
  </div>
</nav>

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

  .links a {
    font-size: 0.95rem;
    font-weight: 500;
    color: var(--color-text-muted);
  }

  .links a:hover {
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
