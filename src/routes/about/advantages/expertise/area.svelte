<script lang="ts">
    export let percentage: number;
    export let title: string;
</script>

<div class="space-y-4">
    <p class="text-zinc-950 font-medium">{title}</p>
    <div class="h-1 bg-zinc-100">
        <div style="width:{percentage}%" class=" h-full percent"></div>
    </div>
</div>
