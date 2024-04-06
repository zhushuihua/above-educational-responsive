<script lang="ts">
    export let links: {
        title: string;
        links: { title: string; href: string }[];
    };
</script>

<div class="text-white space-y-4">
    <p class=" font-bold">{links.title}</p>
    <nav>
        <ul class="space-y-2 text-sm">
            {#each links.links as link}
                <li>
                    <a href={link.href}>{link.title}</a>
                </li>
            {/each}
        </ul>
    </nav>
</div>
