<script lang="ts">
    import Card from '../card.svelte';

    export let from: string;
    export let till = 'present';
    export let title: string;
    export let companyName: string;
    export let link: string;
    export let technologies: string[] = [];
</script>

<Card {technologies}>
    <p
        slot="side"
        class="w-full text-right uppercase font-semibold tracking-wide text-slate-500 text-sm"
    >
        {from} — {till}
    </p>
    <a
        slot="title"
        href={link}
        class="leading-tight text-slate-200 font-semibold group/link text-lg"
        target="_blank"
        aria-label={`${title} at ${companyName} (opens in a new tab)`}
        >{title} | {companyName}</a
    >
    <svelte:fragment slot="description">
        <slot />
    </svelte:fragment>
</Card>
