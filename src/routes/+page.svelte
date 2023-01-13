<script>
  import './index.css'

  import profile from '$lib/assets/profile.jpg'
  import About from '$lib/About.svelte'
  import Toolset from '$lib/Toolset.svelte';
  import Projects from '$lib/Projects.svelte';
  import Contact from '$lib/Contact.svelte';

  const motto = '{/*Tech Enthusiast*/}'
</script>

<div class="flex flex-col justify-center items-center">
  <header class="text-stone-200 flex justify-center items-center">
    <img class="w-96 h-auto" src={profile} alt="profile">
    <div>
      <span>Hi!</span>
      <h1>A. Bilal Akcan</h1>
      <h2>UI / UX Engineer</h2>
      <span>{motto}</span>
    </div>
  </header>
  <main>
    <About/>
    <Toolset/>
    <Projects/>
    <Contact/>
  </main>
</div>

<style>
</style>