<script lang="ts">
  const projects = [
    {name:'PM', link:'https://github.com/bllakcn/project-management', id:crypto.randomUUID()},
    {name:'CP', link:'https://github.com/bllakcn/color-palette-generator', id:crypto.randomUUID()}
  ]
</script>

<section id="projects">
  <h3 class='text-center text-neutral-200 text-xl my-10'>My <span class='highlight-tools relative z-10 text-2xl font-black'>Projects</span></h3>
  <div class="flex gap-5 justify-center">
    {#each projects as project (project.id)}
    <button>
      <a href={project.link} target="_blank" rel="noreferrer">
        <span  class="font-extralight text-2xl bg-stone-400 hover:bg-stone-300 text-black w-14 h-14 rounded-lg flex justify-center items-center">{project.name}</span>
      </a>
    </button>
    {/each}
  </div>
</section>

<style>
  .highlight-tools::before{
  content: '';
  width: 100px;
  height: 20px;
  left: -5px;
  bottom: -4px;
  background-color: rgba(49, 46, 129,.5);
  position: absolute;
  z-index: -1;
}
</style>