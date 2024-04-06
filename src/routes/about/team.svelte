<script>
    import Container from "$lib/components/container.svelte";
    const teamData = [
        { image: "img/team1.jpg", name: "Johne Doe", position: "Creative" },
        { image: "img/team2.jpg", name: "Jennifer", position: "Programmer" },
        { image: "img/team3.jpg", name: "Christen", position: "CEO" },
        { image: "img/team4.jpg", name: "Kerinele Rase", position: "Manager" },
    ];
</script>

<Container>
    <h3 class="mt-16 mb-8">Our Team</h3>
    <div class="grid sm:grid-cols-2 lg:grid-cols-4 text-center gap-4">
        {#each teamData as data}
            <div
                class="space-y-4 bg-zinc-100 pb-6 rounded-lg overflow-clip shadow-lg"
            >
                <img src={data.image} alt={data.name} class="w-full" />
                <p class="font-bold text-xl text-zinc-950 text-center">
                    {data.name}
                </p>
                <p>{data.position}</p>
            </div>
        {/each}
    </div>
</Container>
