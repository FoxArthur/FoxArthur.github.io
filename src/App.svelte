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
  import Experience from "./components/experience.svelte";
  import Lastpage from "./components/lastpage.svelte";
  
  

  onMount(() => {
    // Import the fullpage.js library dynamically
    fullpage('#fullpage', {
      // options here
      autoScrolling: true,
      scrollHorizontally: true,
      verticalCentered:false,
      navigation: true,
      navigationPosition: 'right',
      navigationTooltips: ['Home', 'About Me', 'Education', 'Experience', 'Contact'],
      
    });
    
  });

  

</script>

<EventListener />


<main>
    <div id="fullpage">
      <div class="section ">
        <div class="grid md:grid-cols-2 ">
          <div class="flex items-center justify-center h-screen">
            <h1 class="anim-right title text-slate-200 text-center text-8xl">Arthur Vos</h1>
          </div>
          <div>
            <img class=" invisible h-0 md:h-auto md:visible md:ml-12 md:mt-10 anim-left" width="80%" src="../src/assets/images/coding.svg" alt="svg">
          </div>
        </div>
      </div>
      <div class="section ">
        <div class="flex items-center justify-center h-screen">
          <section>
            <div class=" px-4  md:px-6 lg:px-8">
              <div class="grid grid-cols-1 h-screen lg:grid-cols-2">
                <div class="relative z-10 lg:py-16">
                  <div class="relative h-64 md:h-80 lg:h-full">
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
          
                  <div class="p-8 md:p-16 lg:p-16">
                    <h2 class="text-2xl font-bold md:text-3xl text-slate-200">
                      Who am I?
                    </h2>
          
                    <p class="mt-4 text-slate-300">
                      My name is Arthur Vos i'm a 17 year old Software Development student from The Netherlands.
                      I've been programming for about 4 years now, I started when i was 13 years old and i've been doing it ever since.
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

        <div class="grid md:grid-cols-2 ">
          <div class="flex items-center justify-center h-screen">
            <div class="anim-right3 ">
              <Timeline/>
            </div>
          </div>
          <div>
            <img class="invisible h-0 md:h-auto md:visible ml-12 md:mt-40 anim-left3 rounded-lg shadow-none transition-shadow duration-100 ease hover:shadow-lg hover:shadow-slate-700 cursor-pointer "  width="90%" src="https://www.hoornbeeck.nl/app/uploads/2020/04/2021-10-14-Hoornbeeck-Amersfoort-originele-kwaliteit-165.jpg" alt="svg">
            
          </div>
        </div>
        
      </div>
      <div class="section">
        <div class="flex justify-center items-center">
          <h2 class=" text-slate-200 text-center text-4xl mt-8 anim-right4">Experience</h2>
        </div>
        <Experience/>
      </div>
      <div class="section">
        <Lastpage/>
      </div>
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

.anim-right, .anim-right2, .anim-right3, .anim-right4 {
    opacity: 0;
    filter: blur(5px);
    transform: translateX(-80%);
    
}
.anim-left, .anim-left2, .anim-left3 {
    opacity: 0;
    filter: blur(5px);
    transform: translateX(100%);
    
}





</style>
