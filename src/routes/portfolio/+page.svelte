<script lang="ts">
    import SubHeader from "$lib/components/common/sub-header.svelte";
    import Container from "$lib/components/container.svelte";
    import { fade, scale, slide } from "svelte/transition";
    import images from "./images";
    import { flip } from "svelte/animate";
    import Hilighte from "./hilighte.svelte";
    let filteredImages = images;
    let selectedChecked = 0;
    let selectedIndex = -1;
    let showHilite = false;
    enum category {
        all,
        web,
        mobile,
        design,
    }
    let checked: category = category.all;
    $: switch (checked) {
        case category.all:
            filteredImages = images;
            break;
        case category.web:
            filteredImages = [images[0], images[3], images[4], images[5]];
            break;
        case category.mobile:
            filteredImages = [images[2], images[5]];
            break;
        case category.design:
            filteredImages = [images[1], images[2], images[4], images[7]];
    }
</script>

<SubHeader title="Portfolio"></SubHeader>
<Container>
    <div class="space-x-2 mt-16 text-sm">
        <label
            class="inline-block px-4 py-2.5 border text-teal-400 has-[:checked]:bg-zinc-100"
        >
            <input
                type="radio"
                class="sr-only"
                name="category"
                value={category.all}
                bind:group={checked}
            />
            <span>All</span>
        </label>
        <label
            class="inline-block px-4 py-2.5 border text-teal-400 has-[:checked]:bg-zinc-100"
        >
            <input
                type="radio"
                class="sr-only"
                name="category"
                value={category.web}
                bind:group={checked}
            />
            <span>Web Design</span>
        </label>
        <label
            class="inline-block px-4 py-2.5 border text-teal-400 has-[:checked]:bg-zinc-100"
        >
            <input
                type="radio"
                class="sr-only"
                name="category"
                value={category.mobile}
                bind:group={checked}
            />
            <span>Mobile Apps</span>
        </label>
        <label
            class="inline-block px-4 py-2.5 border text-teal-400 has-[:checked]:bg-zinc-100"
        >
            <input
                type="radio"
                class="sr-only"
                name="category"
                value={category.design}
                bind:group={checked}
            />
            <span>UI Design</span>
        </label>
    </div>
</Container>
<div class="mt-8">
    <Container>
        <div class="grid lg:grid-cols-3 gap-4">
            {#each filteredImages as image, index (image)}
                <div
                    transition:slide={{ axis: "x" }}
                    animate:flip={{ duration: 200 }}
                    class="relative group cursor-pointer"
                    style="perspective: 4000px;"
                >
                    <img src="img/works/{image}" alt="" />
                    <button
                        on:click={() => {
                            selectedIndex = index;
                            showHilite = true;
                        }}
                        class="absolute inset-0 transition-all bg-green-700/65 duration-1000 [transform:rotateY(180deg)_scale(0%)] group-hover:[transform:rotateY(0deg)_scale(100%)] grid place-content-center"
                    >
                        <svg
                            xmlns="http://www.w3.org/2000/svg"
                            fill="none"
                            viewBox="0 0 24 24"
                            stroke-width="3"
                            stroke="currentColor"
                            class="w-6 h-6 text-white animate-pulse"
                        >
                            <path
                                stroke-linecap="round"
                                stroke-linejoin="round"
                                d="M3.75 3.75v4.5m0-4.5h4.5m-4.5 0L9 9M3.75 20.25v-4.5m0 4.5h4.5m-4.5 0L9 15M20.25 3.75h-4.5m4.5 0v4.5m0-4.5L15 9m5.25 11.25h-4.5m4.5 0v-4.5m0 4.5L15 15"
                            />
                        </svg>
                    </button>
                </div>
            {/each}
        </div>
    </Container>
</div>
{#if showHilite}
    <Hilighte {selectedIndex} images={filteredImages} bind:showHilite
    ></Hilighte>
{/if}

<style lang="postcss">
</style>
