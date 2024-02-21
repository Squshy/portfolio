<script lang="ts">
    import { T } from '@threlte/core';
    import { Canvas } from '@threlte/core';
    import { Theatre } from '@threlte/theatre';
    import Knot from './knot.svelte';
</script>

<div class="w-screen z-20 relative h-screen">
    <Theatre studio={{ enabled: true }}>
        <Canvas>
            <T.PerspectiveCamera
                makeDefault
                position={[3, 1.5, -5]}
                on:create={({ ref }) => {
                    ref.lookAt(0, 0, 0);
                }}
                fov={50}
            />
            <T.AmbientLight />
            <Knot key="torus" />
        </Canvas>
    </Theatre>
</div>
