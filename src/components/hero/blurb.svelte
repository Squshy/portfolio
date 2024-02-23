<script lang="ts">
    import { Sequence } from '@threlte/theatre';
    import TheatreTextBox from '../theatre-text-box.svelte';
    import Icon from '../icon.svelte';
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

        <div class="flex flex-col gap-1 justify-center items-center">
            <TheatreTextBox key="hehe" class="flex">
                <h1
                    class="w-full text-center text-lg font-semibold text-white/70"
                >
                    Senior Software Engineer at PostGrid
                </h1>
            </TheatreTextBox>
            <TheatreTextBox key="icons">
                <!-- TODO: Fix the scaling clipping -->
                <div class="flex flex-row gap-2 items-center">
                    <a href="https://github.com/Squshy" target="_blank">
                        <Icon
                            name="GitHub"
                            class="w-8 h-8 flex hover:scale-110 transition duration-100 ease-out fill-white/70 hover:fill-white"
                        />
                    </a>
                    <a
                        href="https://linkedin.com/in/calvin-lapp"
                        target="_blank"
                    >
                        <Icon
                            name="LinkedIn"
                            class="w-8 h-8 flex hover:scale-110 transition duration-100 ease-out fill-white/70 hover:fill-white"
                        />
                    </a>
                </div>
            </TheatreTextBox>
        </div>
    </div>
</div>
