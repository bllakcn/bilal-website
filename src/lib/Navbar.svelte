<script lang="ts">
  export let scrolled: boolean;
</script>

<aside class:scrolled class="text-neutral-400 fixed right-0 text-right p-5 pr-3 hidden lg:block z-10">
  <ul class="mr-5 text-xs leading-loose tracking-wider font-medium">
    <li><a href="#about">About</a></li>
    <li><a href="#toolset">Toolset</a></li>
    <li><a href="#projects">Projects</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
  {#if scrolled}
  <ul class="py-2 mr-5 text-xs leading-loose tracking-wider font-medium">
    <a href="/">
      <li class="flex fill-neutral-400 justify-center items-center">
        <span>Go top</span>
        <svg class="content-center" xmlns="http://www.w3.org/2000/svg" viewBox="-50 -25 100 100" height="36" width="36"><path d="M22.5 40V13.7L10.1 26.1 8 24 24 8l16 16-2.1 2.1-12.4-12.4V40Z"/></svg>
      </li>
    </a>
  </ul>  
  {/if}
</aside>

<style>
  aside {
    transition: all .5s;
    direction: rtl;
    visibility: hidden;
    opacity: 0;
  }
  aside.scrolled{
    visibility: visible;
    opacity: .6;
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
  aside li:hover svg {
    fill: #fff;
  }
</style>