<script lang="ts">
    const textSections = [
        `My name is Sören Möller, and I am a dedicated student currently 
        pursuing a degree in Computer Science at the University of Kassel. 
        This portfolio showcases my academic journey, the skills I have 
        acquired over the years, and a timeline of projects that reflect my 
        diverse interests and rapid learning capabilities.`,
        
        `Throughout my studies, I have developed a strong foundation in
        various programming languages and technologies, complemented by
        hands-on experience in real-world projects. This portfolio serves 
        as a testament to my commitment to continuous learning and 
        adaptability in the ever-evolving field of technology.`,
        
        `I invite you to explore my skills and projects, which not only 
        demonstrate my technical abilities but also my passion for 
        innovative solutions and problem-solving. I am eager to leverage my 
        knowledge and skills in a professional setting, contributing 
        positively to a forward-thinking organization.` 
    ]
</script>

<section id="about-me" class="flex flex-col items-center dark-gray-text text-center">
    <div class="w-64 h-64 rounded-full overflow-hidden transition-transform duration-300 
                    ease-in-out transform hover:scale-[1.1]">
        <img 
        class="w-full h-full object-cover scale-[2.3] object-[-15px_0%] " 
        src="/profile-picture.jpg" 
        alt="Portrait"
        />
    </div>

    <h1 class="mt-8 text-5xl font-bold">Sören Möller</h1>
    <h3 class="mt-4 mb-16 italic text-xl">
        Computer Science Student @ University of Kassel
    </h3>

    {#each textSections as text}
        <p class="mt-4">{text}</p> 
    {/each}
</section> 
