<script lang="ts">
    import Tag from './tag.svelte';

    export let technologies: string[] = [];
</script>

<div class="group hover:bg-[#1e2129] p-8 grid sm:grid-cols-8">
    <div class="w-full sm:col-span-2 px-4 py-2">
        <slot name="side" />
    </div>
    <div class="sm:col-span-6 px-4 py-2">
        <h2 class="font-medium leading-snug">
            <slot name="title" />
        </h2>
        <p class="mt-2 text-md leading-normal"><slot name="description" /></p>
        {#if technologies.length}
            <ul class="mt-2 flex flex-wrap">
                {#each technologies as t}
                    <li class="mr-1.5 mt-2">
                        <Tag>{t}</Tag>
                    </li>
                {/each}
            </ul>
        {/if}
    </div>
</div>
