<script lang="ts">
    import { T } from '@threlte/core';
    import * as THREE from 'three';
    import { SheetObject } from '@threlte/theatre';

    export let key: string;
    const geo = new THREE.TorusKnotGeometry(10, 3, 300, 16);
</script>

<SheetObject {key} let:Transform>
    <Transform>
        <T.Mesh>
            <T.MeshStandardMaterial color="#049ef4" roughness={0.5} />
            <T is={geo} />
        </T.Mesh>
    </Transform>
</SheetObject>
