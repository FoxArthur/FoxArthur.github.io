<head>
  <link rel="stylesheet" type="text/css" href="fullpage.css" />
  <script type="text/javascript" src="fullpage.js"></script>
  <link rel="stylesheet" href="../node_modules/aos/dist/aos.css"/>
</head>

<script>
  import "./app.css";
  import "./animations.css";
  import { onMount } from "svelte";
  import "fullpage.js/dist/fullpage.css";
  import fullpage from "fullpage.js";
  
  

  onMount(() => {
    // Import the fullpage.js library dynamically
    fullpage('#fullpage', {
      // options here
      autoScrolling: true,
      scrollHorizontally: true,
      verticalCentered:false
    });
  });

  document.addEventListener('DOMContentLoaded', () => {
  const observer = new IntersectionObserver(entries => {
    entries.forEach((entry) => {
      if (entry.isIntersecting) {
        entry.target.setAttribute("style", "opacity: 1; filter: blur(0); transform: translateX(0);")
      } else {
        if(entry.target == document.querySelector(".anim")){
          entry.target.setAttribute("style", "opacity: 0; filter: blur(5px); transform: translateX(-100%);")
        } else if(entry.target == document.querySelector(".anim2")){
          entry.target.setAttribute("style", "opacity: 0; filter: blur(5px); transform: translateX(100%);")
        }
      }
    });
  });

  const animElements = document.querySelectorAll(".anim");
  const animElements2 = document.querySelectorAll(".anim2");
  animElements.forEach((el) => observer.observe(el));
  animElements2.forEach((el) => observer.observe(el));
});

</script>
<main>
    <div id="fullpage">
      <div class="section ">
        <div class="grid sm:grid-cols-2 ">
          <div class="flex items-center justify-center h-screen">
            <h1 class="anim title text-slate-200 text-center text-8xl">Arthur Vos</h1>
          </div>
          <div>
            <img class="ml-12 mt-10 anim2" width="80%" src="../src/assets/images/coding.svg" alt="svg">
          </div>
        </div>
      </div>
      <div class="section ">
        <div class="grid sm:grid-cols-2 ">
          <div class="flex items-center justify-center h-screen">
            <div class="anim title text-slate-200 text-center text-8xl">
              <h1
        class="bg-gradient-to-r from-green-300 via-blue-500 to-purple-600 bg-clip-text text-3xl font-extrabold text-transparent sm:text-5xl"
      >
        Understand User Flow.

        <span class="sm:block"> Increase Conversion. </span>
      </h1>
            </div>
          </div>
          <div>
            <div class="ml-12 mt-10 anim2">
              
            </div>
          </div>
        </div>
      </div>
      <div class="section">Some section</div>
      <div class="section">Some section</div>
  </div>
</main>
<style>
  :root{
    background-color: rgb(23, 23, 23);
  }
  h1{
    font-family: league;
  }

  .title {
  box-shadow: inset 0 0 0 0 rgb(23, 23, 23);
  
  margin: 0 -.1rem;
  padding: 0 .1rem;
  padding-top: 1rem;  
  transition: color .6s ease-in-out, box-shadow .5s ease-in-out;
}
.title:hover {
  box-shadow: inset 1000px 0 0 0 rgb(226, 232, 240);
  color: rgb(23, 23, 23);
}

.anim {
    opacity: 0;
    filter: blur(5px);
    transform: translateX(-100%);
    transition: all 1s;
}
.anim2 {
    opacity: 0;
    filter: blur(5px);
    transform: translateX(100%);
    transition: all 1s;
}




</style>
