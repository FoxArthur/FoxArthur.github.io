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
  import EventListener from "./components/eventListener.svelte";
  import Timeline from "./components/timeline.svelte";
  
  

  onMount(() => {
    // Import the fullpage.js library dynamically
    fullpage('#fullpage', {
      // options here
      autoScrolling: true,
      scrollHorizontally: true,
      verticalCentered:false
    });
  });

  

</script>

<EventListener />

<main>
    <div id="fullpage">
      <div class="section ">
        <div class="grid sm:grid-cols-2 ">
          <div class="flex items-center justify-center h-screen">
            <h1 class="anim-right title text-slate-200 text-center text-8xl">Arthur Vos</h1>
          </div>
          <div>
            <img class="ml-12 mt-10 anim-left" width="80%" src="../src/assets/images/coding.svg" alt="svg">
          </div>
        </div>
      </div>
      <div class="section ">
        <div class="flex items-center justify-center h-screen">
          <section>
            <div class=" px-4  sm:px-6 lg:px-8">
              <div class="grid grid-cols-1 h-screen lg:grid-cols-2">
                <div class="relative z-10 lg:py-16">
                  <div class="relative h-64 sm:h-80 lg:h-full">
                    <img
                      alt="House"
                      src="../src/assets/images/gala-crop.jpg"
                      class="anim-right2 absolute inset-0 h-full w-full object-cover"
                    />
                  </div>
                </div>
          
                <div class=" relative flex items-center ">
                  <div class="anim-left2 lg:py-48 bg-neutral-800">
                    <span
                    class="hidden lg:absolute lg:inset-y-0 lg:-start-16 lg:block lg:w-16 lg:bg-neutral-800"
                  ></span>
          
                  <div class="p-8 sm:p-16 lg:p-16">
                    <h2 class="text-2xl font-bold sm:text-3xl text-slate-200">
                      Who am I?
                    </h2>
          
                    <p class="mt-4 text-slate-300">
                      My name is Arthur Vos i'm a 17 year old Software Development student from The Netherlands.
                      I've been programming for about 3 years now, I started when i was 14 years old and i've been doing it ever since.
                      I made this site to show off some of my skills and to tell something about myself.
                    </p>
          
                    
                  </div>
                  </div>
                </div>
              </div>
            </div>
          </section>
          
        </div>
      </div>
      <div class="section">

        <div class="grid sm:grid-cols-2 ">
          <div class="flex items-center justify-center h-screen">
            <div class="anim-right3 ">
              <Timeline/>
            </div>
          </div>
          <div>
            <img class="ml-12 mt-40 anim-left3 rounded-lg shadow-none transition-shadow duration-100 ease hover:shadow-lg hover:shadow-slate-700 cursor-pointer "  width="90%" src="https://www.hoornbeeck.nl/app/uploads/2020/04/2021-10-14-Hoornbeeck-Amersfoort-originele-kwaliteit-165.jpg" alt="svg">
            
          </div>
        </div>
        
      </div>
      <div class="section">
        <div class="flex justify-center items-center">
          <h2 class=" text-slate-200 text-center text-4xl mt-8">Experieces</h2>
      </div>
        <div class="flex justify-center items-center">
          <button class="h-44 w-32 text-slate-200 bg-neutral-800 rounded-xl flex flex-col justify-center shadow duration-300 hover:bg-slate-200 hover:text-neutral-900 hover:shadow-xl">
            <svg class="h-14" fill="#000000" viewBox="0 0 24 24" role="img" xmlns="http://www.w3.org/2000/svg"><g id="SVGRepo_bgCarrier" stroke-width="0"></g><g id="SVGRepo_tracerCarrier" stroke-linecap="round" stroke-linejoin="round"></g><g id="SVGRepo_iconCarrier"><title>C Sharp icon</title><path d="M12 0A12 12 0 000 12a12 12 0 0012 12 12 12 0 0012-12A12 12 0 0012 0zM9.426 7.12a5.55 5.55 0 011.985.38v1.181a4.5 4.5 0 00-2.25-.566 3.439 3.439 0 00-2.625 1.087 4.099 4.099 0 00-1.012 2.906 3.9 3.9 0 00.945 2.754 3.217 3.217 0 002.482 1.023 4.657 4.657 0 002.464-.634l-.004 1.08a5.543 5.543 0 01-2.625.555 4.211 4.211 0 01-3.228-1.297 4.793 4.793 0 01-1.212-3.409 5.021 5.021 0 011.365-3.663 4.631 4.631 0 013.473-1.392 5.55 5.55 0 01.12-.004 5.55 5.55 0 01.122 0zm5.863.155h.836l-.555 2.652h1.661l.567-2.652h.81l-.555 2.652 1.732-.004-.15.697H17.91l-.412 1.98h1.852l-.176.698h-1.816l-.58 2.625h-.83l.567-2.625h-1.65l-.555 2.625h-.81l.555-2.625h-1.74l.131-.698h1.748l.401-1.976h-1.826l.138-.697h1.826zm.142 3.345L15 12.6h1.673l.423-1.98z"></path></g></svg>
            <span class="mt-6 text-sm ?leading-5 font-semibold text-center">Frozen<br>Seafoods</span>
          </button>
          <button class="h-44 w-32 text-slate-200 bg-neutral-800 rounded-xl flex flex-col justify-center shadow duration-300 hover:bg-slate-200 hover:text-neutral-900 hover:shadow-xl">
            <svg xmlns="http://www.w3.org/2000/svg" class="h-14" viewBox="0 0 448 512"><!--! Font Awesome Free 6.4.2 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2023 Fonticons, Inc. --><style>svg{fill:#171717}</style><path d="M243.583 91.6027L323.695 138.384C326.575 140.026 326.68 144.583 323.695 146.225L228.503 201.854C225.623 203.55 222.22 203.444 219.549 201.854L124.357 146.225C121.425 144.636 121.373 139.973 124.357 138.384L204.417 91.6027V0L0 119.417V358.252L78.3843 312.477V218.914C78.3319 215.576 82.2066 213.192 85.0865 214.993L180.279 270.622C183.159 272.318 184.782 275.338 184.782 278.464V389.669C184.834 393.007 180.959 395.391 178.079 393.589L97.9673 346.808L19.583 392.583L224 512L428.417 392.583L350.033 346.808L269.921 393.589C267.093 395.338 263.114 393.06 263.218 389.669V278.464C263.218 275.126 265.051 272.159 267.721 270.622L362.914 214.993C365.741 213.245 369.72 215.47 369.616 218.914V312.477L448 358.252V119.417L243.583 0V91.6027Z"/></svg>
            <span class="mt-6 text-sm ?leading-5 font-semibold text-center">Frozen<br>Seafoods</span>
          </button>
            <button class="h-44 w-32 text-slate-200 bg-neutral-800 rounded-xl flex flex-col justify-center shadow duration-300 hover:bg-slate-200 hover:text-neutral-900 hover:shadow-xl">
              <svg xmlns="http://www.w3.org/2000/svg" class="h-14" viewBox="0 0 448 512"><!--! Font Awesome Free 6.4.2 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2023 Fonticons, Inc. --><style>svg{fill:#171717}</style><path d="M439.8 200.5c-7.7-30.9-22.3-54.2-53.4-54.2h-40.1v47.4c0 36.8-31.2 67.8-66.8 67.8H172.7c-29.2 0-53.4 25-53.4 54.3v101.8c0 29 25.2 46 53.4 54.3 33.8 9.9 66.3 11.7 106.8 0 26.9-7.8 53.4-23.5 53.4-54.3v-40.7H226.2v-13.6h160.2c31.1 0 42.6-21.7 53.4-54.2 11.2-33.5 10.7-65.7 0-108.6zM286.2 404c11.1 0 20.1 9.1 20.1 20.3 0 11.3-9 20.4-20.1 20.4-11 0-20.1-9.2-20.1-20.4.1-11.3 9.1-20.3 20.1-20.3zM167.8 248.1h106.8c29.7 0 53.4-24.5 53.4-54.3V91.9c0-29-24.4-50.7-53.4-55.6-35.8-5.9-74.7-5.6-106.8.1-45.2 8-53.4 24.7-53.4 55.6v40.7h106.9v13.6h-147c-31.1 0-58.3 18.7-66.8 54.2-9.8 40.7-10.2 66.1 0 108.6 7.6 31.6 25.7 54.2 56.8 54.2H101v-48.8c0-35.3 30.5-66.4 66.8-66.4zm-6.7-142.6c-11.1 0-20.1-9.1-20.1-20.3.1-11.3 9-20.4 20.1-20.4 11 0 20.1 9.2 20.1 20.4s-9 20.3-20.1 20.3z"/></svg>
              <span class="mt-6 text-sm ?leading-5 font-semibold text-center">Frozen<br>Seafoods</span>
            </button>
            
        </div>
        

      </div>
      <div class="section">Some section</div>
  </div>
</main>
<style>
  :root{
    background-color: rgb(23, 23, 23);
  }
  h1, h2{
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

.anim-right, .anim-right2, .anim-right3 {
    opacity: 0;
    filter: blur(5px);
    transform: translateX(-100%);
    
}
.anim-left, .anim-left2, .anim-left3 {
    opacity: 0;
    filter: blur(5px);
    transform: translateX(100%);
    
}





</style>
