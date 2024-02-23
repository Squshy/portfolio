<script>
    import ContentWrapper from '../content-wrapper.svelte';
    import Title from '../title.svelte';
    import Card from './card.svelte';
</script>

<ContentWrapper class="flex flex-col gap-4">
    <Title>Projects</Title>
    <Card
        title="Chop DB"
        from="2024"
        till="Present"
        technologies={['Rust', 'Go', 'gRPC']}
        >A distributed, log structured database.</Card
    >
    <Card
        title="Alertle"
        from="2023"
        technologies={[
            'TypeScript',
            'React',
            'Vite',
            'Changelogs',
            'TurboRepo',
        ]}>A <i>blazingly fast</i>🔥 alert library for React.</Card
    >
    <Card
        title="TewDew"
        from="2023"
        technologies={[
            'Rust',
            'GraphQL',
            'Actix Web',
            'TypeScript',
            'React',
            'Urql',
            'Vite',
            'TurboRepo',
        ]}
        >A GraphQL to-do app providing typical CRUD operations powered by a
        stable Rust backend. This app is authenticated with JWT tokens and
        driven by the combination of Urql and React on the frontend.</Card
    >
    <Card
        title="Algorithm Showcase"
        from="2021"
        technologies={['TypeScript', 'NextJS', 'Dijkstra', 'Priority Queues']}
        >A display of different algorithms at work with an interactive Dijkstra
        example which shows how the shortest path algorithm works on an
        interactive grid. This app also showcases how different sorting
        algorithms work by showing the sorts in real-time.</Card
    >
</ContentWrapper>
