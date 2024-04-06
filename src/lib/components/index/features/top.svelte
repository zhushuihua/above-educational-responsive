<section
    class="h-40 top relative before:-skew-y-12 before:translate-x-16 after:-translate-x-16 after:skew-y-12 overflow-clip"
>
    <slot />
</section>

<style lang="postcss">
    .top::before,
    .top::after {
        content: "";
        @apply absolute bottom-0 left-0 h-16 translate-y-14 bg-zinc-100 w-full;
    }
</style>
