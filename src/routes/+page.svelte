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

  import profile from '$lib/assets/profile.jpg'
  import About from '$lib/About.svelte'
  import Toolset from '$lib/Toolset.svelte';
  import Projects from '$lib/Projects.svelte';
  import Contact from '$lib/Contact.svelte';
  import Navbar from '$lib/Navbar.svelte';

  const motto: string = '{/*Tech Enthusiast*/}'
</script>

<svelte:window bind:scrollY={y}/>

<div class="flex flex-col">
  <header class="flex flex-col lg:flex-row justify-center items-center mx-auto lg:mx-0 lg:gap-9" class:scrolled>
    <img class="max-w-xs h-auto p-5 rounded-full" src={profile} alt="profile">
    <div class="text-center lg:text-left lg:mx-32">
      <span class="mb-4 text-3xl tracking-wider text-transparent bg-clip-text bg-gradient-to-b from-stone-400 via-stone -400 to-transparent">Hi!</span>
      <h1 class='text-5xl text-stone-300 mb-4 lg:mb-3'>A. <span class='font-extrabold text-stone-200'>Bilal</span> Akcan</h1>
      <h3 class='p-0 mb-2 tracking-widest text-2xl font-bold text-stone-300'>UI/UX <span class='text-3xl font-black text-transparent bg-clip-text bg-gradient-to-br from-cyan-300 to-indigo-900'>Engineer</span></h3>
      <span class="p-0 m-0 tracking-wide text-l font-mono select-none text-stone-500">{motto}</span>
    </div>
  </header>
  <main class:scrolled class="text-stone-200 bg-black pt-20">
    <About/>
    <Toolset/>
    <Projects/>
    <Contact/>
  </main>
  <Navbar scrolled={scrolled} />
</div>

<style>
  header {
    transition: all .5s;
    height: 100vh;
  }
  header.scrolled {
    height: 0vh;
  }
</style>