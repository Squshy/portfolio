<script lang="ts">
    import { T, useTask } from '@threlte/core';
    import Knot from './knot.svelte';
    // TODO: Make this respond to window resize
    const cameraAspect = window.innerWidth / window.innerHeight;

    let rotation = 0;
    useTask((d) => {
        rotation += d / 2;
    });
</script>

<T.PerspectiveCamera
    makeDefault
    fov={70}
    aspect={cameraAspect}
    near={10}
    far={200}
    position.z={50}
/>
<T.DirectionalLight
    intensity={40}
    color="#FF0000"
    position.y={20}
    position.z={20}
    castShadow
    shadow.mapSize.width={2048}
    shadow.mapSize.height={2048}
    shadow.camera.far={50}
    shadow.camera.near={1}
    shadow.camera.top={20}
    shadow.camera.right={20}
    shadow.camera.bottom={-20}
    shadow.camera.left={-20}
/>
<T.RectAreaLight
    color="FF0"
    width={50}
    height={50}
    position.z={10}
    position.y={-40}
    position.x={-20}
    on:create={({ ref }) => {
        ref.lookAt(0, 0, 0);
    }}
/>
<T.AmbientLight intensity={0.45} />
<Knot key="torus" rotation.y={rotation} />
