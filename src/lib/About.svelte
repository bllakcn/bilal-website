<section id="about" class='relative bg-black text-neutral-300 flex flex-col justify-center items-center pb-16'>
  <div class='absolute md:hidden bg-neutral-800 w-11/12 h-60 left-5 top-2 -rotate-3'></div>
  <h3 class='z-10 text-center text-neutral-200 text-xl my-10'><span class='highlight-about relative z-10 text-2xl font-black'>About</span> Me</h3>
  <div class='z-10 text-center w-11/12 mx-auto max-w-lg'>
    <p><b>Architecture</b> graduate freelancing in <b>tech</b>. Passionate about <b>designing</b> and <b>developing</b> that great <b class='underline decoration-wavy'>user experience</b>.</p>
  </div>
  <!-- <Link className='z-10 mt-5 underline-btn' to='/projects'>Take a look at the projects</Link> -->
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
.underline-btn {
  position: relative;
  font-weight: 500;
}
.underline-btn::after {
  content: '';
  position: absolute;
  width: 2px;
  height: 1px;
  background-color: rgb(212 212 212);
  bottom: 0;
  left: 50%;
  transform: translate(-50%);
  transition: all 250ms;
}
.underline-btn:hover::after {
  content: '';
  position: absolute;
  width: 200px;
  height: 1px;
  background-color: rgb(212 212 212);
  bottom: 0;
  left: 50%;
  transform: translate(-50%);
  animation: hoverUnderline 200ms;
}
</style>