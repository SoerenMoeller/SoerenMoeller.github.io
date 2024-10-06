<script lang="ts">
    const skills = [
        {   
            icon: "fab fa-python",
            title: "Python"
        }
    ] 
</script>

<section id="skills" class="dark-gray py-8 gray-text flex flex-col items-center gap-8">
    <h2 class="text font-bold text-4xl pb-8">Skills</h2> 
    <p class="text-center">
        Over the past few years, I have cultivated a robust set of skills that 
        are essential for my work in technology and software development. 
        Below, you will find a curated selection of key skills I have 
        developed. For more detailed insights into how I have applied these 
        skills, please refer to the Projects section of my portfolio.
        
        I am passionate about continuously learning new technologies, and to 
        maintain a concise overview, some technologies are listed below without 
        extensive elaboration.
    </p>

    <div class="grid grid-cols-1 md:grid-cols-2 xl:grid-cols-3 gap-4 w-full">
        {#each skills as { title, icon }}
            <div class="flex flex-col items-center gap-4">
                <span class="rounded-full flex justify-center items-center 
                    bg-[#242629] w-44 h-44 transition-transform duration-300 
                    ease-in-out transform hover:scale-[1.15]">
                    <i class={`${icon} text-9xl mint-text`}></i>
                </span>
                <h5 class="font-bold text-xl">{title}</h5>
            </div>
        {/each}
    </div>
</section>
