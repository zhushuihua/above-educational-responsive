<script lang="ts">
    import { onDestroy, onMount } from "svelte";
    import { fade, scale } from "svelte/transition";

    const images = ["1.jpg", "2.jpg", "3.jpg"];
    const info = [
        { title: "Online Education", content: "The best educational template" },
        {
            title: "School Education",
            content: "Get all courses with on-line content",
        },
        { title: "Collage Education", content: "Awesome Template get it know" },
    ];
    let index = 0;
    let interval: number = -1;
    onMount(() => {
        interval = setInterval(
            () => (index = (index + 1) % images.length),
            8000,
        );
    });
    onDestroy(() => clearInterval(interval));
</script>

<div class="w-full aspect-video max-h-96 mt-4 relative group">
    {#each images as image, idx}
        {#if idx == index}
            <div
                transition:fade
                class=" absolute w-full h-full"
                class:show-content={idx == index}
            >
                <img
                    src="img/slides/{image}"
                    alt=""
                    class="w-full h-full object-cover"
                />
                <div
                    class="absolute bottom-0 left-0 w-full bg-white/50 grid justify-center items-stretch text-center"
                >
                    <div class="bg-white/80 py-2">
                        <p class="text-zinc-950 text-5xl font-bold px-4 my-2">
                            {info[idx].title}
                        </p>
                        <p class="text-xl text-zinc-950">{info[idx].content}</p>
                    </div>
                    <div class="p-1 space-x-4">
                        <button
                            on:click={() => (index = 0)}
                            class="bg-black/40 w-6 h-2 rounded-full btn"
                            class:btn-selected={index == 0}
                        ></button>
                        <button
                            on:click={() => (index = 1)}
                            class:btn-selected={index == 1}
                            class="bg-black/40 w-6 h-2 rounded-full btn"
                        ></button>
                        <button
                            on:click={() => (index = 2)}
                            class:btn-selected={index == 2}
                            class="bg-black/40 w-6 h-2 rounded-full btn"
                        ></button>
                    </div>
                </div>
            </div>
        {/if}
    {/each}
    <button
        class="group-hover:opacity-100 group-hover:left-1 left-0 arrow"
        on:click={() => {
            if (index > 0) {
                index--;
            } else {
                index = images.length - 1;
            }
        }}
        ><svg
            xmlns="http://www.w3.org/2000/svg"
            fill="none"
            viewBox="0 0 24 24"
            stroke-width="1.5"
            stroke="currentColor"
            class="w-6 h-6 text-zinc-50"
        >
            <path
                stroke-linecap="round"
                stroke-linejoin="round"
                d="M15.75 19.5 8.25 12l7.5-7.5"
            />
        </svg>
    </button>

    <button
        class="group-hover:opacity-100 group-hover:right-1 right-0 arrow"
        on:click={() => {
            index = (index + 1) % images.length;
        }}
        ><svg
            xmlns="http://www.w3.org/2000/svg"
            fill="none"
            viewBox="0 0 24 24"
            stroke-width="1.5"
            stroke="currentColor"
            class="w-6 h-6 text-zinc-50"
        >
            <path
                stroke-linecap="round"
                stroke-linejoin="round"
                d="m8.25 4.5 7.5 7.5-7.5 7.5"
            />
        </svg>
    </button>
</div>

<style lang="postcss">
    .show-content {
        display: block;
    }
    button.arrow {
        @apply p-1 rounded-lg bg-zinc-600 absolute top-1/2 -translate-y-1/2 opacity-0 duration-300 transition-all;
    }
    .btn-selected {
        @apply bg-white;
    }
    .btn {
        @apply transition-all duration-200;
    }
</style>
