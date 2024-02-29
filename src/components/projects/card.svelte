<script lang="ts">
    import Card from '../card.svelte';
    import Icon from '../icon.svelte';

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
    <svelte:fragment slot="title">
        <h3
            class="leading-tight text-slate-200 font-semibold group-hover:text-teal-400 transition ease-out text-lg"
        >
            {title}
        </h3>
        <div class="flex gap-2 mt-2">
            <a
                href={gitHubLink}
                target="_blank"
                aria-label={`${title}'s GitHub (opens in a new tab)`}
                ><Icon
                    name="GitHub"
                    class="w-5 h-5 group-hover:fill-teal-400 fill-slate-500 hover:fill-slate-100 transition ease-out hover:scale-110"
                /></a
            >
            {#if liveLink}
                <a
                    href={liveLink}
                    target="_blank"
                    class="text-slate-500 transition ease-out group-hover:text-teal-400"
                    aria-label={`A live link for ${title} (opens in a new tab)`}
                >
                    <Icon
                        name="External"
                        class="w-5 h-5 hover:scale-110 transition duration-75 ease-out"
                        fill="none"
                        stroke="currentColor"
                        strokeWidth={1.5}
                    />
                </a>
            {/if}
        </div>
    </svelte:fragment>
    <svelte:fragment slot="description">
        <slot />
    </svelte:fragment>
</Card>
