<script>
    import ProjectView from "./ProjectView.svelte";
    
    let active; 
    const projects = [
        {
            title: "Minigames in PyGame",
            preview: "profile-picture.jpg",
        } 
    ] 
</script>


<section id="projects" class="py-8 dark-gray-text flex flex-col items-center gap-8">
    <h2 class="text font-bold text-4xl">Projects</h2> 
    <p class="text-center">
        Over the years I have done a variety of projects. This is a collection
        of them. For the most part, these are chronologically ordered.
        For each of them I add some info, like why I started the project, 
        what the project includes, and what I have learned implementing it. 
        If you are interested in my ability to learn and my motivation behind
        it, this section is for you.
    </p>

    <div class="grid grid-cols-3 justify-between w-full">
        {#each projects as project}
            <div class="flex justify-center w-full grid grid-cols-1 grid-rows-1 gap-2">
                <div class="row-start-1 col-start-1 shadow-lg h-80">
                    <img class="w-full h-80 rounded" alt="Project Preview" src={project.preview}/>
                </div>
                <button 
                    class="row-start-1 col-start-1 shadow-lg h-80 dark-gray 
                    rounded opacity-85 hover:opacity-40 transition duration-500 
                    ease-in-out flex justify-center items-center"
                    on:click={() => active = project}
                >
                    <h5 class="text-4xl gray-text">
                        {project.title}
                    </h5>
                </button>
            </div>
        {/each}
    </div>

    {#if active}
        <ProjectView project={active}/>
    {/if}
</section>
