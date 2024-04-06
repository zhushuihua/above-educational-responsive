<script>
    import Container from "$lib/components/container.svelte";
    import Expertise from "./expertise.svelte";
    import Solution from "./solutions.svelte";
</script>

<Container>
    <div class="mt-16 grid lg:grid-cols-3 gap-4">
        <div class="space-y-4">
            <h2 class="text-2xl font-bold text-zinc-950">Why Choose US?</h2>
            <p>
                Sed ut perspiciaatis unde omnis iste natus error sit voluptatem
                accusantium doloremque laudantium, totam rem aperiam, eaque ipsa
                quae ab illo inventore veritatis et quasi architecto beatae
                vitae dicta sunt explicabo. Nemo enim ipsam voluptatem quia
                voluptas sit aspernatur.
            </p>
            <p>
                Sed ut perspiciaatis iste natus error sit voluptatem probably
                haven't heard of them accusamus.
            </p>
        </div>
        <Solution></Solution>

        <Expertise />
    </div>
</Container>
