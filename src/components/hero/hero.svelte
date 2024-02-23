<script lang="ts">
    import { Canvas } from '@threlte/core';
    import { Theatre, Sheet } from '@threlte/theatre';
    import Scene from './scene.svelte';
    import state from '../animation-state.json';
    import Blurb from './blurb.svelte';
</script>

<div class="w-full h-[100vh] relative">
    <Theatre config={{ state }} studio={{ enabled: false }}>
        <div class="aboslute left-0 top-0 w-screen h-full">
            <Canvas>
                <Scene />
            </Canvas>
        </div>
        <div class="w-full h-full absolute left-0 top-0">
            <div class="w-full h-full flex items-center justify-center">
                <Sheet name="intro">
                    <Blurb />
                </Sheet>
            </div>
        </div>
    </Theatre>
</div>
