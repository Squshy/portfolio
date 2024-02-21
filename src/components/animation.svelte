<script lang="ts">
    import { Canvas } from '@threlte/core';
    import { Theatre } from '@threlte/theatre';
    import Scene from './scene.svelte';
</script>

<div class="w-screen z-20 relative h-screen">
    <Theatre studio={{ enabled: false }}>
        <Canvas>
            <Scene />
        </Canvas>
    </Theatre>
</div>
