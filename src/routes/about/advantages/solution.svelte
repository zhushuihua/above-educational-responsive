<script lang="ts">
    import { slide } from "svelte/transition";

    export let a: string;
    export let q: string;
    let open = false;
</script>

<div
    class="bg-zinc-600 rounded-lg text-white group [&:has(:focus)_p[data-underline]]:underline"
>
    <button
        class=" flex gap-1 items-center p-4"
        on:click={() => (open = !open)}
    >
        <svg
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 24 24"
            fill="currentColor"
            class="w-4 h-4"
        >
            <path
                fill-rule="evenodd"
                d="M16.28 11.47a.75.75 0 0 1 0 1.06l-7.5 7.5a.75.75 0 0 1-1.06-1.06L14.69 12 7.72 5.03a.75.75 0 0 1 1.06-1.06l7.5 7.5Z"
                clip-rule="evenodd"
            />
        </svg>
        <p
            data-underline
            class="group-hover:underline underline-offset-4 uu transition-all"
        >
            {q}
        </p>
    </button>
    {#if open}
        <div class="p-4 bg-zinc-500 border-t" transition:slide>
            <p>{a}</p>
        </div>
    {/if}
</div>
