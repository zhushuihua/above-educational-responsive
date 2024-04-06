<script lang="ts">
    import Container from "$lib/components/container.svelte";
    import { onDestroy, onMount } from "svelte";
    import Quote from "./quote.svelte";
    let selectedIndex = 0;
    const quotes = [
        {
            content:
                "Blanditiis praesentium voluptatum deleniti atque corrupti quos dolores et quas molestias excepturi sint occaecati cupiditate non provident, similique sunt in culpa qui officia deserunt mollitia animi.",
            name: "Mark John",
        },
        {
            content:
                "Blanditiis praesentium voluptatum deleniti atque corrupti quos dolores et quas molestias excepturi sint occaecati cupiditate non provident, similique sunt in culpa qui officia deserunt mollitia animi.",
            name: "Jaison Warner",
        },
        {
            content:
                "Blanditiis praesentium voluptatum deleniti atque corrupti quos dolores et quas molestias excepturi sint occaecati cupiditate non provident, similique sunt in culpa qui officia deserunt mollitia animi.",
            name: "Tony Antonio",
        },
        {
            content:
                "Blanditiis praesentium voluptatum deleniti atque corrupti quos dolores et quas molestias excepturi sint occaecati cupiditate non provident, similique sunt in culpa qui officia deserunt mollitia animi.",
            name: "Leena Doe ",
        },
    ];
    let interval = -1;
    onMount(() => {
        interval = setInterval(() => {
            selectedIndex = (selectedIndex + 1) % quotes.length;
        }, 3000);
    });
    onDestroy(() => clearInterval(interval));
</script>

<div class="bg-zinc-200 my-8 py-8 overflow-clip">
    <Container>
        <div class="overflow-clip">
            <div
                class="flex transition-all"
                style="transform: translateX(-{100 * selectedIndex}%);"
            >
                {#each quotes as quote}
                    <div
                        class="py-4 w-full shrink-0 text-center translate-x-0 transition-all"
                    >
                        <Container>
                            <p>
                                {quote.content}
                            </p>
                            <p class="mt-4 font-bold text-zinc-950">
                                --{quote.name}--
                            </p>
                        </Container>
                    </div>
                {/each}
            </div>
        </div>
        <div class="flex justify-center gap-4 [&_button]:transition-all">
            <button
                on:click={() => (selectedIndex = 0)}
                class="size-2 rounded-full delay-200 border-zinc-400 border"
                class:active={selectedIndex == 0}
            ></button>
            <button
                on:click={() => (selectedIndex = 1)}
                class="size-2 rounded-full delay-200 border-zinc-400 border"
                class:active={selectedIndex == 1}
            ></button>
            <button
                on:click={() => (selectedIndex = 2)}
                class="size-2 rounded-full delay-200 border-zinc-400 border"
                class:active={selectedIndex == 2}
            ></button>
            <button
                on:click={() => (selectedIndex = 3)}
                class="size-2 rounded-full delay-200 border-zinc-400 border"
                class:active={selectedIndex == 3}
            ></button>
        </div>
    </Container>
</div>

<style class="postcss">
    .active {
        @apply bg-white scale-150;
    }
</style>
