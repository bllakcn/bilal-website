<script lang="ts">
  import './index.css'

  let y: number;
  let scrolled: boolean = false;

  $: {
    if(y > 40){
        scrolled = true;
      } else {
        scrolled = false;
      }
  }

  const scrollByArrow = () => {
    y += 42;
  } 

  import profile from '$lib/assets/profile.jpg'
  import About from '$lib/About.svelte'
  import Toolset from '$lib/Toolset.svelte';
  import Projects from '$lib/Projects.svelte';
  import Contact from '$lib/Contact.svelte';
  import Navbar from '$lib/Navbar.svelte';

  const motto: string = '{/*Tech Enthusiast*/}'
</script>

<svelte:window 
  bind:scrollY={y} 
  />


<div class="flex flex-col">
  <header class="relative flex flex-col lg:flex-row justify-center items-center mx-auto lg:mx-0 lg:gap-9 pb-6" class:scrolled>
    <img class="max-w-xs h-auto p-5 rounded-full" src={profile} alt="profile">
    <div class="text-center lg:text-left lg:mx-32">
      <span class="mb-4 text-3xl tracking-wider text-transparent bg-clip-text bg-gradient-to-b from-stone-400 via-stone -400 to-transparent">Hi!</span>
      <h1 class='text-5xl text-stone-300 mb-4 lg:mb-3'>A. <span class='font-extrabold text-stone-200'>Bilal</span> Akcan</h1>
      <h2 class='p-0 mb-2 tracking-widest text-2xl font-bold text-stone-300'>UI/UX <span class='text-3xl font-black text-transparent bg-clip-text bg-gradient-to-br from-cyan-300 to-indigo-900'>Engineer</span></h2>
      <span class="p-0 m-0 tracking-wide text-l font-mono select-none text-stone-500">{motto}</span>
    </div>
    <button on:click={scrollByArrow} class="fill-stone-500 cursor-pointer p-1 absolute bottom-16 lg:bottom-3 w-8" >
      <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512"><path d="M233.4 406.6c12.5 12.5 32.8 12.5 45.3 0l192-192c12.5-12.5 12.5-32.8 0-45.3s-32.8-12.5-45.3 0L256 338.7 86.6 169.4c-12.5-12.5-32.8-12.5-45.3 0s-12.5 32.8 0 45.3l192 192z"/></svg>
    </button>
  </header>
  <main class:scrolled class="text-stone-200 bg-black pt-28 relative">
    <About/>
    <Toolset/>
    <Projects/>
    <Contact/>
  </main>
  <Navbar scrolled={scrolled} />
  <footer class="text-center text-stone-500 select-none">
    <span>© 2022 Ahmet Bilal Akcan</span>
  </footer>
</div>

<style>
  header {
    transition: all .5s;
    height: 100vh;
  }
  header.scrolled {
    height: 0vh;
  }
  svg {
    transition: all .5s;
    opacity: 1;
  }
</style>