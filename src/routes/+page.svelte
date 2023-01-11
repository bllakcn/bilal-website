<script>
  import './index.css'

  import profile from '$lib/assets/profile.jpg'
  import About from '$lib/About.svelte'
  import Toolset from '$lib/Toolset.svelte';
  import Projects from '$lib/Projects.svelte';
  import Contact from '$lib/Contact.svelte';

  const motto = '{/*Tech Enthusiast*/}'
</script>

<div class="wrapper">
  <header>
    <img src={profile} alt="profile">
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
  .wrapper {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }
  header {
    color: #fff;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  img {
    width: 400px;
    height: auto;
  }
</style>