<script lang="ts">
    import Container from "$lib/components/container.svelte";
    export let title: string;
</script>

<div class="h-2 bg-teal-700"></div>
<div class="text-white bg-teal-600 py-8">
    <Container>
        <h2 class="text-3xl font-bold text-white">{title}</h2>
    </Container>
</div>
<svelte:head>
    <title>{title} - UMA Maths</title>
</svelte:head>
