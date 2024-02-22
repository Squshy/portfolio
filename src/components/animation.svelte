<script lang="ts">
    import { Canvas } from '@threlte/core';
    import { Theatre, Sheet } from '@threlte/theatre';
    import Scene from './scene.svelte';
    import state from './knot-state.json';
    import Test from './test.svelte';
</script>

<div class="w-full h-screen z-20 relative">
    <Theatre config={{ state }} studio={{ enabled: true }}>
        <div class="fixed left-0 top-0 w-screen z-10 h-screen">
            <Canvas>
                <Scene />
            </Canvas>
        </div>
        <div class="w-full h-screen fixed z-20 left-0">
            <div class="w-full h-full flex items-center justify-center">
                <Sheet name="intro">
                    <Test />
                </Sheet>
            </div>
        </div>
    </Theatre>
</div>
