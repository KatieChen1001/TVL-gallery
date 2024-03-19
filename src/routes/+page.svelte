<script>
    import { Card, Button, Toggle, Gallery } from "flowbite-svelte";
    import { ArrowRightOutline } from "flowbite-svelte-icons";
    let vCard = false;
    import examples from "../lib/examples.json";
    import Example from "../lib/components/example.svelte";
</script>

<div>
    <div
        class="flex items-center justify-center py-4 md:py-8 flex-wrap gap-3 mb-3 mx-auto"
    >
        <Button pill size="xl" outline>All categories</Button>
        <Button pill size="xl" color="alternative">Bar</Button>
        <Button pill size="xl" color="alternative">Line</Button>
        <Button pill size="xl" color="alternative">Circular</Button>
        <Button pill size="xl" color="alternative">Area</Button>
        <Button pill size="xl" color="alternative">Scatter</Button>
    </div>

    <div class="grid grid-cols-4 md:grid-cols-4 gap-6">
        {#each examples as example}
            <Example chartInfo={example} />
        {/each}
    </div>
</div>
