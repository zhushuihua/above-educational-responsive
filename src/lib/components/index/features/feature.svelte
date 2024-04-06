<script lang="ts">
    import Top from "./top.svelte";

    export let title: string;
    export let content: string;
</script>

<div class=" space-y-4 bg-zinc-100">
    <Top>
        <slot />
    </Top>
    <p class="text-zinc-950 text-3xl font-bold">
        {title}
    </p>
    <p class="p-4">{content}</p>
</div>
