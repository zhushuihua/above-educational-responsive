<script>
    import Container from "$lib/components/container.svelte";
    export let center = true;
</script>

<Container>
    <h2
        class=" font-bold text-3xl text-zinc-950"
        style="text-align:{center ? 'center' : 'auto'};"
    >
        Courses We offser
    </h2>
    <p class="my-4">
        Lorem ipsum dolor sit amet, consectetur adipisicing elit. Dolores quae
        porro consequatur aliquam, incidunt eius magni provident, doloribus
        omnis minus temporibus perferendis nesciunt quam repellendus nulla nemo
        ipsum odit corrupti consequuntur possimus, vero mollitia velit ad
        consectetur. Alias, laborum excepturi nihil autem nemo numquam, ipsa
        architecto non, magni consequuntur quam.
    </p>
    <div class="md:grid-cols-3 grid md:gap-4">
        <div class="p-4 space-y-4 bg-zinc-100">
            <h3 class="text-2xl font-bold text-zinc-950">Heading Course</h3>
            <p>
                Lorem ipsum dolor sit amet, consectetuer adipiscing elit.
                Praesent vest sit amet, consec ibulum molestie lacus. Aenean
                nonummy hendrerit mauris. Phasellus porta.
            </p>
        </div>
        <div class="p-4 space-y-4 bg-zinc-100">
            <h3 class="text-2xl font-bold text-zinc-950">Heading Course</h3>
            <p>
                Lorem ipsum dolor sit amet, consectetuer adipiscing elit.
                Praesent vest sit amet, consec ibulum molestie lacus. Aenean
                nonummy hendrerit mauris. Phasellus porta.
            </p>
        </div>
        <div class="p-4 space-y-4 bg-zinc-100">
            <h3 class="text-2xl font-bold text-zinc-950">Heading Course</h3>
            <p>
                Lorem ipsum dolor sit amet, consectetuer adipiscing elit.
                Praesent vest sit amet, consec ibulum molestie lacus. Aenean
                nonummy hendrerit mauris. Phasellus porta.
            </p>
        </div>
    </div>
    <div class="md:grid-cols-3 grid md:gap-4 mt-4">
        <div class="p-4 space-y-4 bg-zinc-100">
            <h3 class="text-2xl font-bold text-zinc-950">Heading Course</h3>
            <p>
                Lorem ipsum dolor sit amet, consectetuer adipiscing elit.
                Praesent vest sit amet, consec ibulum molestie lacus. Aenean
                nonummy hendrerit mauris. Phasellus porta.
            </p>
        </div>
        <div class="p-4 bg-zinc-100">
            <h3 class="text-2xl font-bold text-zinc-950">Heading Course</h3>
            <p>
                Lorem ipsum dolor sit amet, consectetuer adipiscing elit.
                Praesent vest sit amet, consec ibulum molestie lacus. Aenean
                nonummy hendrerit mauris. Phasellus porta.
            </p>
        </div>
        <div class="p-4 bg-zinc-100">
            <h3 class="text-2xl font-bold text-zinc-950">Heading Course</h3>
            <p>
                Lorem ipsum dolor sit amet, consectetuer adipiscing elit.
                Praesent vest sit amet, consec ibulum molestie lacus. Aenean
                nonummy hendrerit mauris. Phasellus porta.
            </p>
        </div>
    </div>
</Container>
