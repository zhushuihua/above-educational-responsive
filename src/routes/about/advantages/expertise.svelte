<script>
    import Area from "./expertise/area.svelte";
</script>

<div>
    <h2 class="mb-4">Expertise</h2>
    <div class="space-y-6">
        <div class="[&_.percent]:bg-red-500">
            <Area title="Web Development" percentage={30}></Area>
        </div>
        <div class="[&_.percent]:bg-green-500">
            <Area title="Designing" percentage={74}></Area>
        </div>
        <div class="[&_.percent]:bg-sky-500">
            <Area title="User Experience" percentage={64}></Area>
        </div>
        <div class="[&_.percent]:bg-blue-500">
            <Area title="Development" percentage={82}></Area>
        </div>
    </div>
</div>
