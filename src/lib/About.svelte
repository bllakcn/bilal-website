<section id="about" class='relative bg-black text-neutral-300 flex flex-col justify-center items-center pb-16'>
  <div class='absolute md:hidden bg-neutral-800 w-11/12 h-60 left-5 top-2 -rotate-3'></div>
  <h3 class='z-10 text-center text-neutral-200 text-xl my-10'><span class='highlight-about relative z-10 text-2xl font-black'>About</span> Me</h3>
  <div class='z-10 text-center w-11/12 mx-auto max-w-lg'>
    <p><b>Architecture</b> graduate freelancing in <b>tech</b>. Passionate about <b>designing</b> and <b>developing</b> that great <b class='underline decoration-wavy'>user experience</b>.</p>
  </div>
</section>

<style>
  @keyframes hoverUnderline {
  0%{
    width: 0%;
  }
  100%{
    width: 200px;
  }
}

.highlight-about::before{
  content: '';
  width: 70px;
  height: 20px;
  left: -5px;
  bottom: -4px;
  background-color:rgba(49, 46, 129,.5);
  position: absolute;
  z-index: -1;
}
.underline{
  text-decoration-skip-ink: none;
  text-decoration-thickness: .1em;
  text-decoration-color: rgba(6, 182, 212,.9);
}
</style>