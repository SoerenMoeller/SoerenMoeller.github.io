<script lang="ts">
    let headerContainer: HTMLElement;
    const buttons = ["About Me", "Skills", "Academic", "Work", "Projects"];
    const textToId = (text: string) => 
        text.toLowerCase().replace(' ', '-');

    const scrollTo = (id: string) => {
        const mainContainer = document.getElementById("main");
        const element = document.getElementById(id);
        if (!element || !mainContainer) {
            return;
        }

        const position = element.offsetTop - headerContainer.clientHeight;
        mainContainer.scrollTo({
            top: element.offsetTop - headerContainer.clientHeight, 
            behavior: 'smooth'
        });
    };
</script>

<header 
    bind:this={headerContainer} 
    class="flex h-[8%] items-center justify-between dark-gray"
>
    <div class="mint p-2 rounded hidden md:block">Sören Möller</div>
    <nav class="flex gap-2 md:gap-8 justify-between w-full md:w-auto">
        {#each buttons as content}
            <button 
                on:click={() => scrollTo(textToId(content))} 
                class="mint-text text-center text-sm md:text-base"
            >
                {content}
            </button>
        {/each}
    </nav>
</header>
