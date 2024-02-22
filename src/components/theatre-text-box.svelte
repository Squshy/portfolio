<script lang="ts">
    // @see: https://github.com/threlte/threlte/blob/main/apps/docs/src/components/Hero/Intro/TheatreTextBox.svelte
    // TODO: Figure out why I have to import it like this? Some config maybe? idk
    import * as THEATRE from '@theatre/core';
    const types = THEATRE.types;
    import { createSheetObjectAction } from '@threlte/theatre';
    import Reveal from './reveal.svelte';
    import FadeOut from './fade-out.svelte';

    const sheetObject = createSheetObjectAction();

    export let key: string;
    let reveal = 0;
    let fade = 0;
</script>

<div
    {...$$restProps}
    use:sheetObject={{
        key,
        props: {
            opacity: types.number(1, {
                range: [0, 1],
            }),
            translateX: types.number(0, {
                range: [-100, 100],
            }),
            translateY: types.number(0, {
                range: [-100, 100],
            }),
            reveal: types.number(0, {
                range: [0, 1],
            }),
            fade: types.number(0, {
                range: [0, 1],
            }),
        },
        callback(node, props) {
            node.style.opacity = props.opacity;
            node.style.transform = `translate(${props.translateX}px, ${props.translateY}px)`;
            reveal = props.reveal;
            fade = props.fade;
        },
    }}
>
    <Reveal progress={reveal}>
        <FadeOut progress={fade}>
            <slot />
        </FadeOut>
    </Reveal>
</div>
