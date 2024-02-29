<script lang="ts">
    import Card from '../card.svelte';
    type PastTitle = {
        name: string;
        from: string;
        till: string;
    };

    export let from: string;
    export let till = 'present';
    export let title: string;
    export let companyName: string;
    export let link: string;
    export let pastTitles: PastTitle[] = [];
    export let technologies: string[] = [];
</script>

<Card {technologies}>
    <ul
        slot="side"
        class="w-full text-right font-semibold tracking-wide text-slate-500 text-sm"
    >
        <li>
            <p class="uppercase">{from} — {till}</p>
        </li>
        {#each pastTitles as pastTitle}
            <li class="mt-2">
                <p class="uppercase">
                    {pastTitle.from} — {pastTitle.till}
                </p>
                <p class="text-xs italic">{pastTitle.name}</p>
            </li>
        {/each}
    </ul>
    <a
        slot="title"
        href={link}
        class="leading-tight text-slate-200 font-semibold group/link text-lg group-hover:text-teal-400 transition ease-out"
        target="_blank"
        aria-label={`${title} at ${companyName} (opens in a new tab)`}
        >{title} | {companyName}</a
    >
    <svelte:fragment slot="description">
        <slot />
    </svelte:fragment>
</Card>
