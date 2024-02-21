<script lang="ts">
    import { T } from '@threlte/core';
    import { OrbitControls } from '@threlte/extras';
    import { SheetObject } from '@threlte/theatre';
</script>

<T.PerspectiveCamera position={[0, 5, 10]} makeDefault>
    <OrbitControls target={{ y: 1.5 }} />
</T.PerspectiveCamera>

<!-- Box -->
<SheetObject key="Box" let:Transform let:Sync>
    <Transform>
        <T.Mesh receiveShadow castShadow position.y={0.5}>
            <T.BoxGeometry args={[1, 1, 1]} />
            <T.MeshStandardMaterial color="#b00d03">
                <Sync color roughness metalness />
            </T.MeshStandardMaterial>
        </T.Mesh>
    </Transform>
</SheetObject>
