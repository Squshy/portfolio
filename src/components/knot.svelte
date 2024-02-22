<script lang="ts">
    import { T } from '@threlte/core';
    import * as THREE from 'three';
    import { SheetObject } from '@threlte/theatre';

    // TODO: Figure out how to type and pass props correctly for $$restProps
    export let key: string;
    export let materialColor = new THREE.Color('#049ef4');
    const geo = new THREE.TorusKnotGeometry(10, 3, 300, 16);
</script>

<SheetObject {key} let:Transform let:Sync>
    <Transform>
        <T.Mesh castShadow receiveShadow {...$$restProps}>
            <T.MeshStandardMaterial
                color={materialColor}
                roughness={0.5}
                transparent
            >
                <Sync color roughness metalness />
            </T.MeshStandardMaterial>
            <T is={geo} />
        </T.Mesh>
    </Transform>
</SheetObject>
