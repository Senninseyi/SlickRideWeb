<script lang="ts">
    const currentYear = new Date().getFullYear();
</script>

<footer>
    <div class="container footer-content">
        <div class="brand">
            <span class="logo-text">Slick Ride</span>
            <p>Redefining urban mobility.</p>
        </div>

        <div class="links">
            <div class="column">
                <h4>Product</h4>
                <a href="#rider">Rider App</a>
                <a href="#driver">Driver App</a>
                <a href="#safety">Safety</a>
            </div>
            <div class="column">
                <h4>Company</h4>
                <a href="#about">About</a>
                <a href="#careers">Careers</a>
                <a href="#contact">Contact</a>
            </div>
            <div class="column">
                <h4>Legal</h4>
                <a href="#privacy">Privacy</a>
                <a href="#terms">Terms</a>
            </div>
        </div>
    </div>
    <div class="container bottom-bar">
        <p>
            &copy; {currentYear} Slick Ride / Remo Rides. All rights reserved.
        </p>
    </div>
</footer>

<style>
    footer {
        padding: 80px 0 40px;
        background: #020202;
        border-top: 1px solid rgba(255, 255, 255, 0.05);
    }

    .footer-content {
        display: flex;
        justify-content: space-between;
        flex-wrap: wrap;
        gap: 48px;
        margin-bottom: 60px;
    }

    .logo-text {
        font-family: var(--font-heading);
        font-weight: 800;
        font-size: 1.5rem;
        color: #fff;
        margin-bottom: 16px;
        display: block;
    }

    .brand p {
        color: var(--color-text-muted);
        max-width: 300px;
    }

    .links {
        display: flex;
        gap: 64px;
        flex-wrap: wrap;
    }

    .column h4 {
        color: #fff;
        margin-bottom: 24px;
        font-size: 0.9rem;
        text-transform: uppercase;
        letter-spacing: 0.05em;
    }

    .column a {
        display: block;
        color: var(--color-text-muted);
        margin-bottom: 12px;
        font-size: 0.95rem;
    }

    .column a:hover {
        color: var(--color-primary);
    }

    .bottom-bar {
        border-top: 1px solid rgba(255, 255, 255, 0.05);
        padding-top: 32px;
        text-align: center;
        color: rgba(255, 255, 255, 0.3);
        font-size: 0.9rem;
    }
</style>
