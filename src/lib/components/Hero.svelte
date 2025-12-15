<script lang="ts">
</script>

<section class="hero">
    <div class="container hero-content">
        <h1>
            The Future of <br />
            <span class="gradient-text">Urban Mobility</span>
        </h1>
        <p class="subtitle">
            Join the Ride (Remo Rides) ecosystem. Seamless, sustainable, and
            slick.
        </p>
        <div class="actions">
            <button class="btn-primary">Download App</button>
            <button class="btn-secondary">Learn More</button>
        </div>
    </div>

    <div class="hero-bg">
        <div class="glow glow-1"></div>
        <div class="glow glow-2"></div>
    </div>
</section>

<style>
    .hero {
        position: relative;
        min-height: 100vh;
        display: flex;
        align-items: center;
        padding-top: var(--header-height);
        overflow: hidden;
    }

    .hero-content {
        position: relative;
        z-index: 10;
        text-align: center;
        display: flex;
        flex-direction: column;
        align-items: center;
        gap: 24px;
        max-width: 800px;
    }

    h1 {
        font-size: 4rem;
        font-weight: 800;
        line-height: 1.1;
        letter-spacing: -0.03em;
    }

    .subtitle {
        font-size: 1.25rem;
        color: var(--color-text-muted);
        max-width: 600px;
    }

    .actions {
        display: flex;
        gap: 16px;
        margin-top: 16px;
    }

    button {
        padding: 14px 28px;
        border-radius: 100px;
        font-size: 1rem;
        font-weight: 600;
        transition: all 0.2s ease;
    }

    .btn-primary {
        background: var(--color-primary);
        color: #000;
        box-shadow: 0 0 20px var(--color-primary-glow);
    }

    .btn-primary:hover {
        transform: translateY(-2px);
        box-shadow: 0 0 40px var(--color-primary-glow);
    }

    .btn-secondary {
        background: rgba(255, 255, 255, 0.05);
        color: #fff;
        border: 1px solid rgba(255, 255, 255, 0.1);
    }

    .btn-secondary:hover {
        background: rgba(255, 255, 255, 0.1);
        border-color: rgba(255, 255, 255, 0.2);
    }

    /* Background Effects */
    .hero-bg {
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        z-index: 1;
        pointer-events: none;
    }

    .glow {
        position: absolute;
        border-radius: 50%;
        filter: blur(100px);
        opacity: 0.5;
    }

    .glow-1 {
        width: 500px;
        height: 500px;
        background: var(--color-primary);
        top: -100px;
        right: -100px;
        animation: float 10s ease-in-out infinite;
    }

    .glow-2 {
        width: 600px;
        height: 600px;
        background: var(--color-secondary);
        bottom: -100px;
        left: -200px;
        animation: float 15s ease-in-out infinite reverse;
    }

    @keyframes float {
        0% {
            transform: translate(0, 0);
        }
        50% {
            transform: translate(50px, 50px);
        }
        100% {
            transform: translate(0, 0);
        }
    }

    @media (max-width: 768px) {
        h1 {
            font-size: 3rem;
        }
    }
</style>
