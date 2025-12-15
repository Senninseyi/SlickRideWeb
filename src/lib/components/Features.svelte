<script lang="ts">
    const features = [
        {
            title: "Rider App",
            desc: "Get where you need to go with style and speed. Real-time tracking and premium rides.",
            icon: "🚗",
        },
        {
            title: "Driver Connect",
            desc: "Empowering drivers with tools to maximize earnings and manage trips effortlessly.",
            icon: "⚡",
        },
        {
            title: "Smart Ecosystem",
            desc: "Integrated platform for seamless communication between riders, drivers, and operations.",
            icon: "🌐",
        },
    ];
</script>

<section id="features" class="features">
    <div class="container">
        <div class="section-header">
            <h2>The <span class="gradient-text">Ecosystem</span></h2>
            <p>Everything you need for a modern transportation experience.</p>
        </div>

        <div class="grid">
            {#each features as feature}
                <div class="card">
                    <div class="icon">{feature.icon}</div>
                    <h3>{feature.title}</h3>
                    <p>{feature.desc}</p>
                </div>
            {/each}
        </div>
    </div>
</section>

<style>
    .features {
        padding: 100px 0;
        position: relative;
        background: linear-gradient(to bottom, var(--color-bg), #08080a);
    }

    .section-header {
        text-align: center;
        margin-bottom: 60px;
    }

    h2 {
        font-size: 2.5rem;
        margin-bottom: 16px;
    }

    .section-header p {
        color: var(--color-text-muted);
        font-size: 1.1rem;
    }

    .grid {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
        gap: 24px;
    }

    .card {
        background: rgba(255, 255, 255, 0.03);
        border: 1px solid rgba(255, 255, 255, 0.05);
        padding: 32px;
        border-radius: 24px;
        transition: all 0.3s ease;
    }

    .card:hover {
        background: rgba(255, 255, 255, 0.05);
        transform: translateY(-5px);
        border-color: rgba(255, 255, 255, 0.1);
        box-shadow: 0 10px 30px rgba(0, 0, 0, 0.5);
    }

    .icon {
        font-size: 2rem;
        margin-bottom: 24px;
        background: rgba(255, 255, 255, 0.05);
        width: 64px;
        height: 64px;
        display: flex;
        align-items: center;
        justify-content: center;
        border-radius: 16px;
    }

    h3 {
        font-size: 1.5rem;
        margin-bottom: 12px;
    }

    p {
        color: var(--color-text-muted);
        font-size: 0.95rem;
    }
</style>
