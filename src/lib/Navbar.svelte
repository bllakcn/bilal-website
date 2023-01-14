<script lang="ts">
  let y: number;
  let scrolled: boolean = false;

  $: {
    if(y > 100){
        scrolled = true;
      } else {
        scrolled = false;
      }
  }
  
</script>

<svelte:window bind:scrollY={y}/>
<aside class:scrolled class="text-stone-400 fixed right-0 text-right p-5 pr-3 hidden lg:block">
  <ul class="list-disc list-inside">
    <li><a href="#about">About</a></li>
    <li><a href="#toolset">Toolset</a></li>
    <li><a href="#projects">Projects</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
</aside>

<style>
  aside {
    transition: all .5s;
    direction: rtl;
  }
  aside.scrolled{
    opacity: .5;
  }
  aside.scrolled:hover {
    opacity: 1;
  }
  aside li {
    position: relative;
    transition: all .1s;
  }
  aside li:hover {
    color: #fff;
  }
</style>