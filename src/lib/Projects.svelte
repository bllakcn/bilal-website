<script lang="ts">
  const projects = [
    {
      name:'PM',
      title:'Project Management App',
      details:'Create, track your projects & collaborate',
      link:'https://github.com/bllakcn/project-management',
      bgColor: '#9b718d',
      id:crypto.randomUUID()
    },
    {
      name:'CP',
      title:'Color Palette Generator',
      details:'A lightweight color palette generator',
      link:'https://github.com/bllakcn/color-palette-generator',
      bgColor: '#86a9b4',
      id:crypto.randomUUID()
    }
  ]
</script>

<section id="projects">
  <h3 class='text-center text-neutral-200 text-xl my-10'>My <span class='highlight-projects relative z-10 text-2xl font-black'>Projects</span></h3>
  <div class="flex flex-col sm:flex-row gap-5 justify-center items-left mx-auto max-w-xs sm:max-w-max">
    {#each projects as project (project.id)}
    <button style="--bg-color:{project.bgColor}" class="hover:bg-neutral-800 transition-all rounded-xl p-2 relative">
      <a href={project.link} target="_blank" rel="noreferrer" class="flex justify-start items-center gap-2">
        <span class="font-extralight text-2xl text-black w-14 h-14 rounded-lg flex justify-center items-center">{project.name}</span>
        <div class="text-left">
          <h4 class="font-medium">{project.title}</h4>
          <p class="font-thin text-xs">{project.details}</p>
        </div>
        <svg class="fill-neutral-600 lg:hover:fill-neutral-500 transition-all" xmlns="http://www.w3.org/2000/svg" viewBox="-50 0 100 100" height="48" width="48"><path d="M9 42q-1.2 0-2.1-.9Q6 40.2 6 39V9q0-1.2.9-2.1Q7.8 6 9 6h13.95v3H9v30h30V25.05h3V39q0 1.2-.9 2.1-.9.9-2.1.9Zm10.1-10.95L17 28.9 36.9 9H25.95V6H42v16.05h-3v-10.9Z"/></svg>
      </a>
    </button>
    {/each}
  </div>
</section>

<style>
  .highlight-projects::before{
  content: '';
  width: 110px;
  height: 20px;
  left: -5px;
  bottom: -4px;
  background-color: rgba(49, 46, 129,.5);
  position: absolute;
  z-index: -1;
  color: #9b718d;
}
button span {
  background-color: var(--bg-color);
  filter: saturate(.5);
}
button:hover span {
  filter: saturate(1);
}
</style>