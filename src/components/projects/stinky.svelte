<script>
    import ContentWrapper from '../content-wrapper.svelte';
    import Title from '../title.svelte';
    import Card from './card.svelte';
</script>

<ContentWrapper class="flex flex-col gap-4">
    <Title>Projects</Title>
    <Card
        title="Chop DB"
        gitHubLink="https://github.com/Squshy/chop-db"
        from="2024"
        till="Present"
        technologies={['Rust', 'Go', 'gRPC']}
        >A distributed, log structured key-value store. Similar to Redis, this
        database allows for quick retrieval and storage of persisted key-value
        pairs. This project incorporates ideas presented in the book <a
            href="https://dataintensive.net/"
            target="_blank"
            class="text-teal-100 hover:text-teal-200 transition duration-50 ease-out italic"
            aria-label="Designing Data Intensive applications website (opens in new page)."
            >Designing Data Intensive Applications</a
        > by Martin Fowler.</Card
    >
    <Card
        title="Alertle"
        gitHubLink="https://github.com/Squshy/alertle"
        liveLink="https://www.npmjs.com/package/@alertle/react"
        from="2023"
        technologies={[
            'TypeScript',
            'React',
            'Vite',
            'Vitest',
            'Changelogs',
            'TurboRepo',
        ]}
        >A <i>blazingly fast</i>🔥 alert library for React applications. This
        library incorporates a pub-sub model to update state in deeply nested
        components without causing app wide re-renders.</Card
    >
    <Card
        title="TewDew"
        gitHubLink="https://github.com/Squshy/TewDew"
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
        gitHubLink="https://github.com/Squshy/algorithm-showcase"
        liveLink="https://algorithms.calvinlapp.ca/"
        from="2021"
        technologies={['TypeScript', 'NextJS', 'Dijkstra', 'Priority Queues']}
        >A display of different algorithms at work with an interactive Dijkstra
        example which shows how the shortest path algorithm works on an
        interactive grid. This app also showcases how different sorting
        algorithms work by showing the sorts in real-time.</Card
    >
    <p class="text-center text-sm">
        These are a select few projects, more are listed on my <a
            href="https://github.com/Squshy"
            target="_blank"
            aria-label="My personal GitHub (opens in a new page)."
            class="text-teal-100 hover:text-teal-200 transition duration:50 ease-out"
            >GitHub</a
        >.
    </p>
</ContentWrapper>
