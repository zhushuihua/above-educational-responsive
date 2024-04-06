<script lang="ts">
    import Container from "$lib/components/container.svelte";

    const courseData = [
        {
            image: "img/service1.jpg",
            title: "Web Development",
            content:
                "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Dolores quae porro consequatur aliquam, incidunt eius magni provident, doloribus omnis minus temporibus perferendis nesciunt quam repellendus nulla nemo ipsum odit corrupti consequuntur possimus",
        },
        {
            image: "img/service2.jpg",
            title: "Mobile Development",
            content:
                "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Dolores quae porro consequatur aliquam, incidunt eius magni provident, doloribus omnis minus temporibus perferendis nesciunt quam repellendus nulla nemo ipsum odit corrupti consequuntur possimus",
        },
        {
            image: "img/service3.jpg",
            title: "Responsive Design",
            content:
                "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Dolores quae porro consequatur aliquam, incidunt eius magni provident, doloribus omnis minus temporibus perferendis nesciunt quam repellendus nulla nemo ipsum odit corrupti consequuntur possimus",
        },
    ];
</script>

<Container>
    <div class="grid gap-8 xl:grid-cols-3">
        {#each courseData as data}
            <div class="space-y-4">
                <img src={data.image} alt="" />
                <p class="font-bold text-zinc-950">{data.title}</p>
                <p class="text-sm">{data.content}</p>
            </div>
        {/each}
    </div>
</Container>
