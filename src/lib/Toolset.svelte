<script>
  import reactlogo from './assets/react.png'
  import sveltelogo from './assets/svelte.png'
  import vuelogo from './assets/vue.png'
  import htmllogo from './assets/html.png'
  import csslogo from './assets/css.png'
  import jslogo from './assets/js.png'
  import tailwindlogo from './assets/tailwind.png'
  import pslogo from './assets/ps.png'
  import ailogo from './assets/ai.png'
  import lrlogo from './assets/lr.png'
  import xdlogo from './assets/xd.png'
  import splinelogo from './assets/spline.png'
  import sasslogo from './assets/sass.png'

  const frontSkills = [
  {name:htmllogo, id:1},
  {name:csslogo, id:2},
  {name:jslogo, id:3},
  {name:reactlogo, id:4},
  {name:sveltelogo, id:5},
  {name:vuelogo, id:6},
  {name:sasslogo, id:7},
  {name:tailwindlogo, id:8}
]
const contentSkills = [
  {name:pslogo, id:1},
  {name:ailogo, id:2},
  {name:xdlogo, id:3},
  {name:lrlogo, id:4},
  {name:splinelogo, id:5}
]
</script>

<section id="toolset" class='bg-black text-neutral-300 flex flex-col justify-center pb-16'>
  <h2 class='text-center text-neutral-200 text-xl my-10'>My <span class='highlight-tools relative z-10 text-2xl font-black'>Toolset</span></h2>
  <div class='mx-auto text-center'>
    <p class='font-thin mx-6 text-sm tracking-widest'>Front-end development</p>
    <div class='grid ml-0 p-4 grid-cols-8 gap-5 grey-filtered'>
      {#each frontSkills as frontSkill (frontSkill.id)}
        <img class="w-12"src={frontSkill.name} alt={frontSkill.name}>
      {/each}
    </div>
  </div>
  <div class='mx-auto text-center'>
    <p class='font-thin mx-6 text-sm tracking-widest'>Content Creation</p>
    <div class='grid ml-0 p-4 grid-cols-5 gap-5 grey-filtered'>
      {#each contentSkills as contentSkill (contentSkill.id)}
      <img class="w-12"src={contentSkill.name} alt={contentSkill.name}>
    {/each}
    </div>
  </div>
</section>

<style>
  .grey-filtered img{
  filter: grayscale(95%);
  transition: filter .2s ease-out;
}
.grey-filtered img:hover{
  filter: grayscale(0);
}
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