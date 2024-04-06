<script lang="ts">
    import { fade, scale } from "svelte/transition";

    export let selectedIndex: number;
    export let showHilite: boolean;
    export let images: string[];
    function cancel(evt: KeyboardEvent) {
        if (evt.code === "Escape") {
            showHilite = false;
        }
    }
</script>

<!-- svelte-ignore a11y-click-events-have-key-events -->
<!-- svelte-ignore a11y-no-static-element-interactions -->
<div
    class="fixed inset-0 bg-zinc-800/80 grid place-content-center p-8 z-50"
    transition:fade
    on:click={() => (showHilite = false)}
>
    <div
        class=" max-w-3xl relative group pb-4"
        on:click|preventDefault|stopPropagation
        transition:scale
    >
        <div class=" overflow-clip">
            <div
                class=" flex transition-all ease-in-out"
                style="transform:translateX(-{100 * selectedIndex}%);"
            >
                {#each images as image}
                    <img
                        src="img/works/{image}"
                        alt=""
                        class="w-full shrink-0"
                    />
                {/each}
            </div>
            <p class="p-2 bg-teal-600 text-white">UMA Maths</p>
        </div>
        <button
            class="absolute top-2 right-2 bg-zinc-800 rounded-full p-1 text-white duration-300 opacity-5 group-hover:opacity-100 hover:scale-105 active:scale-90"
            on:click={() => (showHilite = false)}
        >
            <svg
                xmlns="http://www.w3.org/2000/svg"
                fill="none"
                viewBox="0 0 24 24"
                stroke-width="1.5"
                stroke="currentColor"
                class="w-6 h-6"
            >
                <path
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    d="M6 18 18 6M6 6l12 12"
                />
            </svg>
        </button>
        <button
            class="absolute top-1/2 right-0 text-white ps-1 pe-4 py-2 bg-zinc-700 opacity-5 transition-all group-hover:opacity-100 rounded-l-rounded -translate-y-1/2"
            on:click={() =>
                (selectedIndex = (selectedIndex + 1) % images.length)}
        >
            <svg
                xmlns="http://www.w3.org/2000/svg"
                fill="none"
                viewBox="0 0 24 24"
                stroke-width="1.5"
                stroke="currentColor"
                class="w-6 h-6"
            >
                <path
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    d="m12.75 15 3-3m0 0-3-3m3 3h-7.5M21 12a9 9 0 1 1-18 0 9 9 0 0 1 18 0Z"
                />
            </svg>
        </button>
        <button
            class="absolute top-1/2 left-0 text-white ps-4 pe-1 py-2 bg-zinc-700 opacity-5 transition-all group-hover:opacity-100 rounded-l-rounded -translate-y-1/2"
            on:click={() => {
                if (selectedIndex > 0) {
                    selectedIndex--;
                } else {
                    selectedIndex = images.length - 1;
                }
            }}
        >
            <svg
                xmlns="http://www.w3.org/2000/svg"
                fill="none"
                viewBox="0 0 24 24"
                stroke-width="1.5"
                stroke="currentColor"
                class="w-6 h-6"
            >
                <path
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    d="m11.25 9-3 3m0 0 3 3m-3-3h7.5M21 12a9 9 0 1 1-18 0 9 9 0 0 1 18 0Z"
                />
            </svg>
        </button>
    </div>
</div>
<svelte:window on:keydown={cancel} />
