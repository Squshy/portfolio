<script lang="ts">
    import { Canvas } from '@threlte/core';
    import { Theatre } from '@threlte/theatre';
    import Scene from './scene.svelte';
    import state from './knot-state.json';
</script>

<div class="w-full h-full">
    <Theatre config={{ state }} studio={{ enabled: false }}>
        <Canvas>
            <Scene />
        </Canvas>
    </Theatre>
</div>
