<script lang="ts">
    //import Pricing from "$lib/components/landing/Pricing.svelte";
    import type { PageData } from "../pricing/$types";
    import { marked } from "marked";
    import requirements from "$lib/md/requirements.md?raw";
    let htmlContent = marked(requirements);
    export let data: PageData;
</script>

<main class="max-w-screen-md my-20 container mx-auto markdown">
    {@html htmlContent}
</main>

<style>
    :global(h1) {
        font-size: 2rem;
        font-weight: bold;
        margin: 1em 0 0.5em;
    }

    :global(h2) {
        font-size: 1.75rem;
        font-weight: bold;
        margin: 1em 0 0.5em;
    }

    :global(h3) {
        font-size: 1.5rem;
        font-weight: bold;
        margin: 1em 0 0.5em;
    }

    :global(h4) {
        font-size: 1.25rem;
        font-weight: bold;
        margin: 1em 0 0.5em;
    }

    :global(h5) {
        font-size: 1rem;
        font-weight: bold;
        margin: 1em 0 0.5em;
    }

    :global(ul) {
        padding-left: 1.5em;
        margin: 0.5em 0;
    }

    :global(li) {
        margin-bottom: 0.3em;
        line-height: 1.5;
    }

    :global(hr) {
        border: none;
        border-top: 1px solid #ccc;
        margin: 2em 0;
    }
</style>
