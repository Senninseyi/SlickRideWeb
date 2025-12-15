<script lang="ts">
    import Navbar from "$lib/components/Navbar.svelte";
    import Hero from "$lib/components/Hero.svelte";
    import Features from "$lib/components/Features.svelte";
    import Footer from "$lib/components/Footer.svelte";
</script>

<Navbar />
<main>
    <Hero />
    <Features />
</main>
<Footer />

<style>
    main {
        overflow: hidden; /* To contain background glows */
    }
</style>
