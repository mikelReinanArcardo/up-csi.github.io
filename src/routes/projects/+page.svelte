<script lang="ts">
    import FaqItem from '$lib/components/accordions/Accordion.svelte';
    import FaqPanel from '$lib/components/panels/AccordionPanel.svelte';
    import Projects from '$lib/components/panels/ProjectPanel.svelte';
    import ProjectsHeader from '$lib/components/headers/ProjectsHeader.svelte';

    const { data } = $props();
    const { projects, filteredProjects } = $derived(data);
</script>

<ProjectsHeader />

<section class="prose flex flex-col gap-4 lg:flex-row">
    <div class="grow">
        <Projects {projects} {filteredProjects} />
    </div>
</section>

<section>
    <h1 class="border-csi-blue text-foreground mb-8 border-b-3 pb-4 text-3xl font-bold">FAQs</h1>

    <FaqPanel>
        <FaqItem title="What kind of projects can I commission?">
            <span>UP CSI is open to accepting web development projects as of the moment. </span>
        </FaqItem>
        <FaqItem title="How much do projects usually cost?">
            <span
                >Costs vary depending on the scale of the project and the customer’s budget. Prices
                are usually negotiable as projects made with UP CSI is also a way for its members to
                practice the skills they have learned.</span
            >
        </FaqItem>
        <FaqItem title="Who will work on my project?">
            <span
                >The Director of Engineering and the Vice President for Service decide who will work
                on the projects. Priority is given to members who haven’t participated in a service
                project yet. However, these members must have completed the Dev Training Program and
                DevCamp — unless they already have sufficient development experience. UP CSI
                members, who are mostly passionate students from the UP Diliman Department of
                Computer Science, make up the pool of candidates for these projects.</span
            >
        </FaqItem>
    </FaqPanel>
</section>
