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
  <h3 class='text-center text-neutral-200 text-xl my-10'>My <span class='highlight-tools relative z-10 text-2xl font-black'>Projects</span></h3>
  <div class="flex flex-col sm:flex-row gap-5 justify-center items-left mx-auto max-w-xs sm:max-w-max">
    {#each projects as project (project.id)}
    <button style="--bg-color:{project.bgColor}" class="hover:bg-stone-800 transition-all rounded-lg p-2">
      <a href={project.link} target="_blank" rel="noreferrer" class="flex justify-start items-center gap-2">
        <span class="font-extralight text-2xl text-black w-14 h-14 rounded-lg flex justify-center items-center">{project.name}</span>
        <div class="text-left">
          <h4 class="font-medium">{project.title}</h4>
          <p class="font-thin text-xs">{project.details}</p>
        </div>
      </a>
    </button>
    {/each}
  </div>
</section>

<style>
  .highlight-tools::before{
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