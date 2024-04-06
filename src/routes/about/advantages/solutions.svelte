<script lang="ts">
    import Solution from "./solution.svelte";

    const qas = [
        {
            q: " Accordion Heading Text Item # 1",
            a: "Sed ut perspiciaatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsa quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt explicabo. Nemo enim ipsam voluptatem quia voluptas",
        },
        {
            q: " Accordion Heading Text Item # 2",
            a: "Sed ut perspiciaatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsa quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt explicabo. Nemo enim ipsam voluptatem quia voluptas",
        },
        {
            q: " Accordion Heading Text Item # 2",
            a: "Sed ut perspiciaatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsa quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt explicabo. Nemo enim ipsam voluptatem quia voluptas",
        },
        {
            q: " Accordion Heading Text Item # 2",
            a: "Sed ut perspiciaatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsa quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt explicabo. Nemo enim ipsam voluptatem quia voluptas",
        },
    ];
</script>

<div class="space-y-4">
    <h2>Our Solution</h2>
    {#each qas as q}
        <Solution {...q}></Solution>
    {/each}
</div>
