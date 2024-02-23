<script>
    import JobCard from './card.svelte';
    import ContentWrapper from '../content-wrapper.svelte';
    import Title from '../title.svelte';
</script>

<ContentWrapper class="flex flex-col gap-4">
    <Title>Experience</Title>
    <JobCard
        title="Senior Software Engineer"
        companyName="PostGrid"
        link="https://postgrid.com"
        from="Sept 2023"
        technologies={['TypeScript', 'React', 'Express', 'MongoDB', 'Rust']}
        >Hey there. Just gonna put some random jargon here for a lil bit to take
        up some space I guess. I did some stuff</JobCard
    >
    <JobCard
        title="Backend Engineer"
        companyName="PostGrid"
        link="https://postgrid.com"
        from="Feb 2022"
        till="Sept 2023"
        technologies={['TypeScript', 'React', 'Express', 'MongoDB', 'Rust']}
        >Hey there. Just gonna put some random jargon here for a lil bit to take
        up some space I guess. I did some stuff</JobCard
    >
    <JobCard
        title="React Native Developer"
        companyName="A.I. Hub, Durham College"
        link="https://durhamcollege.ca/about/office-of-research-services-innovation-and-entrepreneurship-orsie"
        from="Feb 2022"
        till="Sept 2023"
        technologies={['JavaScript', 'React Native', 'Express', 'MongoDB']}
        >Hey there. Just gonna put some random jargon here for a lil bit to take
        up some space I guess. I did some stuff</JobCard
    >
    <JobCard
        title="Front-End Engineer"
        companyName="A.I. Hub, Durham College"
        link="https://durhamcollege.ca/about/office-of-research-services-innovation-and-entrepreneurship-orsie"
        from="Feb 2022"
        till="Sept 2023"
        technologies={['JavaScript', 'React']}
    >
        Hey there. Just gonna put some random jargon here for a lil bit to take
        up some space I guess. I did some stuff
    </JobCard>
</ContentWrapper>
