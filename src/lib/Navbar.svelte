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
  <ul class="mr-5 text-xs leading-loose tracking-wider font-medium">
    <li><a href="#about">About</a></li>
    <li><a href="#toolset">Toolset</a></li>
    <li><a href="#projects">Projects</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
  {#if scrolled}
  <ul class="py-2 mr-5 text-xs leading-loose tracking-wider font-medium">
    <li><a class="" href="/">Go top</a></li>
  </ul>  
  {/if}
</aside>

<style>
  aside {
    transition: all .5s;

    direction: rtl;
  }
  aside.scrolled{
    opacity: .5;
    padding: .5rem auto;
  }
  aside.scrolled ul {
    line-height: 1;
  }
  aside.scrolled:hover {
    opacity: 1;
  }
  aside li {
    position: relative;
    transition: all .1s;
    transition: line-height .3s;
  }
  aside li:hover {
    color: #fff;
  }
</style>