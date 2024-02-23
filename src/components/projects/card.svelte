<script lang="ts">
    import Card from '../card.svelte';

    // TODO: Figure out why these types aren't yelling at me if one is not
    // provided? I have strict mode on idk
    export let from: string;
    export let till: string;
    export let title: string;
    export let liveLink: string | undefined;
    export let gitHubLink: string;
    export let technologies: string[] = [];
</script>

<Card {technologies}>
    <p
        slot="side"
        class="w-full text-right uppercase font-semibold tracking-wide text-slate-500 text-sm"
    >
        {from}
        {#if till}
            - {till}
        {/if}
    </p>
    <a
        slot="title"
        href={gitHubLink}
        class="leading-tight text-slate-200 font-semibold group/link text-lg"
        target="_blank"
        aria-label={`Personal project titled ${title} (opens in a new tab)`}
        >{title}</a
    >
    <svelte:fragment slot="description">
        <slot />
    </svelte:fragment>
</Card>
