<script lang="ts">
    const achievements = [
        {
            title: "Started at the University of Kassel",
            date: "01.10.2019",
            description: "Started studying Computer Science"
        },
        {
            title: "Bachelor of Science",
            date: "08.11.2022",
            description: `Graduated with a Bachelor of Science in Computer 
                Science from the University of Kassel with an overall grade 
                of 1.3`
        },
        {
            title: "Recipient of Award for Best Graduate of the Year",
            date: "26.05.2023",
            description: `Awarded the "Förderpreis des Fachbereichs 
                Elektrotechnik/Informatk und des VDE Bezirksvereines Kassel e.V." 
                for graduating as the top student (overall grade) of both 
                Computer Science and Electrical Engineering of that year.`
        }, 
        {
            title: "Contributing Author to Research Paper (CADE)",
            date: "09.2023",
            description: `Co-authored a research paper on automated reasoning 
            over experiments (collection of continous functions), presented at 
            the Conference on Automated Deduction (CADE) in September 2023.`,
            link: "https://doi.org/10.1007/978-3-031-38499-8"
        },
        {
            title: "Contributing Author to Research Paper (TIME)",
            date: "09.2023",
            description: `Co-authored a research paper on automated reasoning 
            over experiments that evolve over time, presented at 
            the International Symposium on Temporal Representation and 
            Reasoning (TIME) in September 2023.`,
            link: "https://doi.org/10.4230/LIPIcs.TIME.2023.10"
        }, 
        {
            title: "Contributing Author to Research Presentation (RP)",
            date: "09.2024",
            description: `Co-authored a research presentation on automated 
            reasoning over 2-dimensonal experiments, showcased at the Reachability 
            Problems (RP) conference in September 2024.`
        },
        {
            title: "Expected Graduation with Master of Science in Computer Science",
            date: "Expected: 03.2025",
            description: `Anticipating graduation with a Master of Science in 
            Computer Science from the University of Kassel, with an expected 
            overall grade of 1.0.`
        }
    ];

    const widthTimeline = 'w-3/12 md:w-2/12 pr-2 md:pl-2 xl:pr-0 xl:pl-0';
    const widthAchievement = 'w-9/12 md:w-5/12 pr-2 md:pl-2 xl:pr-0 xl:pl-0';
</script>

<section id="academic" class="py-8 dark-gray-text flex flex-col items-center gap-8">
    <h2 class="text font-bold text-4xl">Academic</h2> 
    <p>A short timeline of my university life.</p>

    <div class="grid grid-rows-1 grid-cols-1 w-full">
        <div class="col-start-1 row-start-1 flex justify-center md:justify-end">
            <div class={`${widthTimeline} flex justify-center`}>
                <div class="h-full w-1 dark-gray"></div> 
            </div>
            <div class={`${widthAchievement} h-4`}></div>
        </div>
        <div class="col-start-1 row-start-1 flex flex-col gap-28">
            {#each achievements as { title, description, date, link}, index}
                <div 
                    class="flex justify-center md:justify-end"
                    class:md:flex-row-reverse={index % 2 == 0}>
                    <div 
                        class:justify-center={index != achievements.length - 1 && index != 0} 
                        class:justify-end={index == achievements.length - 1} 
                        class:justify-start={index == 0} 
                        class={`${widthTimeline} flex items-center flex-col`}
                    >
                        <div class="w-full max-w-40 aspect-square">
                            <div class="p-3 md:p-4 xl:p-6 w-full aspect-square rounded-full dark-gray flex justify-center items-center">
                                <div class="w-full aspect-square rounded-full mint 
                                    transition-transform duration-300 ease-in-out 
                                    transform hover:scale-[1.15]"
                                >
                                </div> 
                            </div> 
                        </div>
                    </div>
                    
                    <div class={`${widthAchievement} flex`}
                        class:md:justify-end={index % 2 == 0}>
                        <div class="flex flex-col h-full justify-center xl:w-11/12 2xl:w-2/3">
                            <h6 
                                class="font-bold text-xl"
                                class:md:text-end={index % 2 == 0}
                            >
                                {title}
                            </h6>
                            <ul class:md:text-end={index % 2 == 0}>
                                <li class="text-lg">{date}</li>
                                <li>
                                    {description} 
                                    {#if link}
                                        <a 
                                            href={link}
                                            class="underline text-[#9fbdb0] hover:text-[#b8d2c4]"
                                        >[link]</a>
                                    {/if}
                                </li>
                            </ul>
                        </div> 
                    </div>
                </div>
            {/each}
        </div>
</section>

