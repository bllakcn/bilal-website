<main class="bg-black text-stone-400 flex justify-center items-center">
  <h1 class="text-center text-neutral-200 text-xl my-10 font-mono">404 <span class="highlight-error relative z-10 text-2xl">not found</span></h1>
</main>

<style>
  main {
    min-height: 100vh;
  }
  .highlight-error::before{
  content: '';
  width: 130px;
  height: 20px;
  left: -5px;
  bottom: -4px;
  background-color:rgba(49, 46, 129,.5);
  position: absolute;
  z-index: -1;
}
</style>