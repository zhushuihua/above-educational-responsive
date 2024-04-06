<script lang="ts">
    import { slide } from "svelte/transition";
    import Container from "../container.svelte";
    import MainNav from "./main-nav.svelte";
    let showMenu = false;
    export let menuHeight: number = 0;
</script>

<Container>
    <header class="py-4">
        <nav class="flex items-center justify-between">
            <a href="#/"> <img src="img/logo.png" alt="" /></a>
            <div class="md:[&_ul]:flex [&_ul]:hidden [&_ul]:gap-4">
                <MainNav />
            </div>
            <button
                on:click={() => (showMenu = !showMenu)}
                class=" md:hidden p-2 border rounded-lg bg-zinc-100 transition-all hover:bg-zinc-200 hover:text-zinc-900 active:scale-95"
                ><svg
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
                        d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5"
                    />
                </svg>
            </button>
        </nav>
    </header>
    {#if showMenu}
        <div
            class:show-menu={showMenu}
            bind:clientHeight={menuHeight}
            transition:slide
        >
            <MainNav />
        </div>
    {/if}
</Container>

<style lang="postcss">
    .show-menu {
        @apply block md:hidden ps-4;
    }
</style>
