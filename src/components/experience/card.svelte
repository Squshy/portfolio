<script lang="ts">
    export let from: string;
    export let till = 'present';
    export let title: string;
    export let companyName: string;
    export let link: string;
</script>

<div class="group hover:bg-[#1e2129] p-12 grid sm:grid-cols-8">
    <!-- Date -->
    <div class="w-full sm:col-span-2 px-4 py-2">
        <p
            class="w-full text-right uppercase font-semibold tracking-wide text-slate-500 text-sm"
        >
            {from} — {till}
        </p>
    </div>
    <div class="sm:col-span-6 px-4 py-2">
        <h2 class="font-medium leading-snug">
            <a
                href={link}
                class="leading-tight text-slate-200 font-semibold group/link text-lg"
                target="_blank"
                aria-label={`${title} at ${companyName} (opens in a new tab)`}
                >{title} | {companyName}</a
            >
        </h2>
        <p class="mt-2 text-md leading-normal"><slot /></p>
    </div>
</div>
