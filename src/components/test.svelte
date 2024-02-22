<script lang="ts">
    import { Sequence } from '@threlte/theatre';
    import TheatreTextBox from './theatre-text-box.svelte';
</script>

<Sequence autoplay />

<div class="w-full flex flex-col">
    <div
        class="max-w-[460px] flex flex-col self-center justify-center items-center"
    >
        <TheatreTextBox key="name" class="flex">
            <h1 class="w-full text-center text-6xl font-bold text-white/80">
                <span class="w-full relative inline-block uppercase rounded-lg">
                    Calvin Lapp
                </span>
            </h1>
        </TheatreTextBox>

        <TheatreTextBox key="hehe" class="flex">
            <h1 class="w-full text-center text-2xl font-bold text-white/80">
                Software Engineer
            </h1>
        </TheatreTextBox>
    </div>
</div>
