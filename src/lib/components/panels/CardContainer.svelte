<script lang="ts">
    import type { Snippet } from 'svelte';

    interface Props {
        text: Snippet;
        cards: Snippet;
    }

    const { text, cards }: Props = $props();
</script>

<div
    class="bg-muted text-muted-foreground flex flex-col items-center justify-between gap-12 rounded-3xl px-8 py-8 transition-colors ease-in-out md:px-24 md:py-16 xl:flex-row"
>
    <div class="flex flex-1 flex-col gap-4 *:!m-0 *:transition-colors *:ease-in-out">
        {@render text()}
    </div>
    <div
        class="flex w-5/6 flex-col justify-center gap-4 *:transition-colors *:ease-in-out md:flex-row xl:w-1/2"
    >
        {@render cards()}
    </div>
</div>
