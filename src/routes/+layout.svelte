<script>
    import Footer from "$lib/components/common/footer/footer.svelte";
    import Header from "$lib/components/common/header.svelte";
    import ScrollToTop from "$lib/components/common/scroll-to-top.svelte";
    import "../app.css";
</script>

<Header />
<slot />
<Footer />
<ScrollToTop />
<svelte:head>
    <title>Above Education</title>
</svelte:head>
