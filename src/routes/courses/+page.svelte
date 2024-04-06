<script>
    import SubHeader from "$lib/components/common/sub-header.svelte";
    import Container from "$lib/components/container.svelte";
    import Courses from "$lib/components/index/courses/courses.svelte";
    import DetailCourse from "./detail-course.svelte";
</script>

<SubHeader title="Courses"></SubHeader>
<div class="my-16">
    <Courses center={false} />
</div>
<Container>
    <p class="mb-8">
        Lorem ipsum dolor sit amet, consectetur adipisicing elit. Dolores quae
        porro consequatur aliquam, incidunt eius magni provident, doloribus
        omnis minus temporibus perferendis nesciunt quam repellendus nulla nemo
        ipsum odit corrupti consequuntur possimus
    </p>
</Container>
<DetailCourse></DetailCourse>
