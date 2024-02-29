<script>
    import Card from './card.svelte';
    import ContentWrapper from '../content-wrapper.svelte';
    import Title from '../title.svelte';
</script>

<ContentWrapper class="flex flex-col gap-4">
    <Title>Experience</Title>
    <Card
        title="Senior Software Engineer"
        companyName="PostGrid"
        pastTitles={[
            { name: 'Backend Engineer', from: 'Feb 2022', till: 'Sept 2023' },
        ]}
        link="https://postgrid.com"
        from="Sept 2022"
        technologies={[
            'TypeScript',
            'React',
            'NodeJS',
            'Express',
            'MongoDB',
            'Rust',
            'Python',
            'Docker',
            'AWS',
        ]}
        >Maintained, built, and shipped production code for vital business
        products servicing millions of API requests daily. Designed and led the
        implementation of new core large scale features from start to finish.
        Enhanced front-end reliability by implementing a comprehensive test
        suite. Maintained and built third party integrations including HubSpot
        and Stripe. Mentored and provided leadership with co-op engineers
        through collaboration and knowledge shares.</Card
    >
    <Card
        title="React Native Developer"
        companyName="A.I. Hub, Durham College"
        link="https://durhamcollege.ca/about/office-of-research-services-innovation-and-entrepreneurship-orsie"
        from="Feb 2022"
        till="Sept 2023"
        technologies={[
            'JavaScript',
            'React Native',
            'NodeJS',
            'Express',
            'MongoDB',
        ]}
        >Collaborated with other students to build a social media native mobile
        application for a local client.
    </Card>
    <Card
        title="Front-End Engineer"
        companyName="A.I. Hub, Durham College"
        link="https://durhamcollege.ca/about/office-of-research-services-innovation-and-entrepreneurship-orsie"
        from="Feb 2022"
        till="Sept 2023"
        technologies={['JavaScript', 'React']}
    >
        Developed a web portal for a health care client, working with external
        APIs to populate and consume patient information.
    </Card>
</ContentWrapper>
