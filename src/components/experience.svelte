<script>
  import { slide } from 'svelte/transition';

document.addEventListener('DOMContentLoaded', () => {
  const observer = new IntersectionObserver(entries => {
    entries.forEach((entry) => {
      if (entry.isIntersecting) {
        if(entry.target == document.querySelector(".anim-right") || entry.target == document.querySelector(".anim-right2") || entry.target == document.querySelector(".anim-right3") || entry.target == document.querySelector(".anim-right4") || entry.target == document.querySelector(".anim-left") || entry.target == document.querySelector(".anim-left2") || entry.target == document.querySelector(".anim-left3")){
          entry.target.setAttribute("style", "opacity: 1; filter: blur(0); transform: translateX(0); transition: all 1s;")
        } else if(entry.target == document.querySelector(".pr-button")){
          entry.target.setAttribute("style", "opacity: 1; filter: blur(0); transform: translateX(0); transition: all 1s; ")
        }else if(entry.target == document.querySelector(".pr-button2")){
          entry.target.setAttribute("style", "opacity: 1; filter: blur(0); transform: translateX(0); transition: all 1s; transition-delay: 200ms; ")
        }else if(entry.target == document.querySelector(".pr-button3")){
          entry.target.setAttribute("style", "opacity: 1; filter: blur(0); transform: translateX(0); transition: all 1s; transition-delay: 300ms; ")
        }else if(entry.target == document.querySelector(".pr-button4")){
          entry.target.setAttribute("style", "opacity: 1; filter: blur(0); transform: translateX(0); transition: all 1s; transition-delay: 400ms; ")
        }else if(entry.target == document.querySelector(".pr-button5")){
          entry.target.setAttribute("style", "opacity: 1; filter: blur(0); transform: translateX(0); transition: all 1s; transition-delay: 500ms; ")
        }else if(entry.target == document.querySelector(".pr-button6")){
          entry.target.setAttribute("style", "opacity: 1; filter: blur(0); transform: translateX(0); transition: all 1s; transition-delay: 600ms; ")
        }
        
      } else {
        if(entry.target == document.querySelector(".anim-right") || entry.target == document.querySelector(".anim-right2") || entry.target == document.querySelector(".anim-right3") || entry.target == document.querySelector(".pr-button") || entry.target == document.querySelector(".pr-button2") ||entry.target == document.querySelector(".pr-button3") || entry.target == document.querySelector(".pr-button4") ||entry.target == document.querySelector(".pr-button5") || entry.target == document.querySelector(".pr-button6") || entry.target == document.querySelector(".timeline-right3")){
          entry.target.setAttribute("style", "opacity: 0; filter: blur(5px); transform: translateX(-100%); ")
        } else if(entry.target == document.querySelector(".anim-left") || entry.target == document.querySelector(".anim-left2") || entry.target == document.querySelector(".anim-left3")){
          entry.target.setAttribute("style", "opacity: 0; filter: blur(5px); transform: translateX(100%);")
        } else if(entry.target == document.querySelector(".anim-right4"))
        {
          entry.target.setAttribute("style", "opacity: 0; filter: blur(5px); transform: translateX(-400%); ")
        }

      }
    });
  });

  
    const prButton = document.querySelectorAll(".pr-button");
    const prButton2 = document.querySelectorAll(".pr-button2");
    const prButton3 = document.querySelectorAll(".pr-button3");
    const prButton4 = document.querySelectorAll(".pr-button4");
    const prButton5 = document.querySelectorAll(".pr-button5");
    const prButton6 = document.querySelectorAll(".pr-button6");

    prButton.forEach((el) => observer.observe(el));
    prButton2.forEach((el) => observer.observe(el));
    prButton3.forEach((el) => observer.observe(el));
    prButton4.forEach((el) => observer.observe(el));
    prButton5.forEach((el) => observer.observe(el));
    prButton6.forEach((el) => observer.observe(el));
    

});

let activeSection = '';

function showSection(section) {
  if(activeSection == "csharp" || activeSection == "unity" || activeSection == "python" || activeSection == "php" || activeSection == "javascript" || activeSection == "other")
  {
    activeSection = "";
    section = '';
    
  }
  
  if(activeSection == "")
    activeSection = section;
  
  
  
  
}

</script>

<div class="flex justify-center items-center mt-10">
    <!-- C# -->
    <div class="pr-button ">
      <button on:click={() => showSection('csharp')} class="mr-10  h-44 w-32 text-slate-200 bg-neutral-800 rounded-xl flex flex-col justify-center shadow duration-300 hover:bg-slate-200 hover:text-neutral-900 hover:shadow-xl">
        <svg class="h-14" fill="#000000" viewBox="0 0 24 24" role="img" xmlns="http://www.w3.org/2000/svg"><g id="SVGRepo_bgCarrier" stroke-width="0"></g><g id="SVGRepo_tracerCarrier" stroke-linecap="round" stroke-linejoin="round"></g><g id="SVGRepo_iconCarrier"><title>C Sharp icon</title><path d="M12 0A12 12 0 000 12a12 12 0 0012 12 12 12 0 0012-12A12 12 0 0012 0zM9.426 7.12a5.55 5.55 0 011.985.38v1.181a4.5 4.5 0 00-2.25-.566 3.439 3.439 0 00-2.625 1.087 4.099 4.099 0 00-1.012 2.906 3.9 3.9 0 00.945 2.754 3.217 3.217 0 002.482 1.023 4.657 4.657 0 002.464-.634l-.004 1.08a5.543 5.543 0 01-2.625.555 4.211 4.211 0 01-3.228-1.297 4.793 4.793 0 01-1.212-3.409 5.021 5.021 0 011.365-3.663 4.631 4.631 0 013.473-1.392 5.55 5.55 0 01.12-.004 5.55 5.55 0 01.122 0zm5.863.155h.836l-.555 2.652h1.661l.567-2.652h.81l-.555 2.652 1.732-.004-.15.697H17.91l-.412 1.98h1.852l-.176.698h-1.816l-.58 2.625h-.83l.567-2.625h-1.65l-.555 2.625h-.81l.555-2.625h-1.74l.131-.698h1.748l.401-1.976h-1.826l.138-.697h1.826zm.142 3.345L15 12.6h1.673l.423-1.98z"></path></g></svg>
        <span class="mt-6 text-sm ?leading-5 font-semibold text-center">C#</span>
      </button>
    </div>
    <!-- Unity -->
    <div class="pr-button2 ">
      <button on:click={() => showSection('unity')} class="mr-10  h-44  w-32 text-slate-200 bg-neutral-800 rounded-xl flex flex-col justify-center shadow duration-300 hover:bg-slate-200 hover:text-neutral-900 hover:shadow-xl">
        <svg xmlns="http://www.w3.org/2000/svg" class="h-14" viewBox="0 0 448 512"><!--! Font Awesome Free 6.4.2 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2023 Fonticons, Inc. --><style>svg{fill:#171717}</style><path d="M243.583 91.6027L323.695 138.384C326.575 140.026 326.68 144.583 323.695 146.225L228.503 201.854C225.623 203.55 222.22 203.444 219.549 201.854L124.357 146.225C121.425 144.636 121.373 139.973 124.357 138.384L204.417 91.6027V0L0 119.417V358.252L78.3843 312.477V218.914C78.3319 215.576 82.2066 213.192 85.0865 214.993L180.279 270.622C183.159 272.318 184.782 275.338 184.782 278.464V389.669C184.834 393.007 180.959 395.391 178.079 393.589L97.9673 346.808L19.583 392.583L224 512L428.417 392.583L350.033 346.808L269.921 393.589C267.093 395.338 263.114 393.06 263.218 389.669V278.464C263.218 275.126 265.051 272.159 267.721 270.622L362.914 214.993C365.741 213.245 369.72 215.47 369.616 218.914V312.477L448 358.252V119.417L243.583 0V91.6027Z"/></svg>
        <span class="mt-6 text-sm ?leading-5 font-semibold text-center">Unity</span>
      </button>
    </div>
    <!-- Python -->
      <div class="pr-button3 ">
        <button on:click={() => showSection('python')} class="mr-10  h-44  w-32 text-slate-200 bg-neutral-800 rounded-xl flex flex-col justify-center shadow duration-300 hover:bg-slate-200 hover:text-neutral-900 hover:shadow-xl">
          <svg xmlns="http://www.w3.org/2000/svg" class="h-14" viewBox="0 0 448 512"><!--! Font Awesome Free 6.4.2 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2023 Fonticons, Inc. --><style>svg{fill:#171717}</style><path d="M439.8 200.5c-7.7-30.9-22.3-54.2-53.4-54.2h-40.1v47.4c0 36.8-31.2 67.8-66.8 67.8H172.7c-29.2 0-53.4 25-53.4 54.3v101.8c0 29 25.2 46 53.4 54.3 33.8 9.9 66.3 11.7 106.8 0 26.9-7.8 53.4-23.5 53.4-54.3v-40.7H226.2v-13.6h160.2c31.1 0 42.6-21.7 53.4-54.2 11.2-33.5 10.7-65.7 0-108.6zM286.2 404c11.1 0 20.1 9.1 20.1 20.3 0 11.3-9 20.4-20.1 20.4-11 0-20.1-9.2-20.1-20.4.1-11.3 9.1-20.3 20.1-20.3zM167.8 248.1h106.8c29.7 0 53.4-24.5 53.4-54.3V91.9c0-29-24.4-50.7-53.4-55.6-35.8-5.9-74.7-5.6-106.8.1-45.2 8-53.4 24.7-53.4 55.6v40.7h106.9v13.6h-147c-31.1 0-58.3 18.7-66.8 54.2-9.8 40.7-10.2 66.1 0 108.6 7.6 31.6 25.7 54.2 56.8 54.2H101v-48.8c0-35.3 30.5-66.4 66.8-66.4zm-6.7-142.6c-11.1 0-20.1-9.1-20.1-20.3.1-11.3 9-20.4 20.1-20.4 11 0 20.1 9.2 20.1 20.4s-9 20.3-20.1 20.3z"/></svg>
          <span class="mt-6 text-sm ?leading-5 font-semibold text-center">Python</span>
        </button>
      </div>
      <!-- PHP -->
      <div class="pr-button4 ">
        <button on:click={() => showSection('php')} class="mr-10  h-44  w-32 text-slate-200 bg-neutral-800 rounded-xl flex flex-col justify-center shadow duration-300 hover:bg-slate-200 hover:text-neutral-900 hover:shadow-xl">
          <svg xmlns="http://www.w3.org/2000/svg" class="h-14" viewBox="0 0 640 512"><!--! Font Awesome Free 6.4.2 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2023 Fonticons, Inc. --><style>svg{fill:#171717}</style><path d="M320 104.5c171.4 0 303.2 72.2 303.2 151.5S491.3 407.5 320 407.5c-171.4 0-303.2-72.2-303.2-151.5S148.7 104.5 320 104.5m0-16.8C143.3 87.7 0 163 0 256s143.3 168.3 320 168.3S640 349 640 256 496.7 87.7 320 87.7zM218.2 242.5c-7.9 40.5-35.8 36.3-70.1 36.3l13.7-70.6c38 0 63.8-4.1 56.4 34.3zM97.4 350.3h36.7l8.7-44.8c41.1 0 66.6 3 90.2-19.1 26.1-24 32.9-66.7 14.3-88.1-9.7-11.2-25.3-16.7-46.5-16.7h-70.7L97.4 350.3zm185.7-213.6h36.5l-8.7 44.8c31.5 0 60.7-2.3 74.8 10.7 14.8 13.6 7.7 31-8.3 113.1h-37c15.4-79.4 18.3-86 12.7-92-5.4-5.8-17.7-4.6-47.4-4.6l-18.8 96.6h-36.5l32.7-168.6zM505 242.5c-8 41.1-36.7 36.3-70.1 36.3l13.7-70.6c38.2 0 63.8-4.1 56.4 34.3zM384.2 350.3H421l8.7-44.8c43.2 0 67.1 2.5 90.2-19.1 26.1-24 32.9-66.7 14.3-88.1-9.7-11.2-25.3-16.7-46.5-16.7H417l-32.8 168.7z"/></svg>
          <span class="mt-6 text-sm ?leading-5 font-semibold text-center">PHP</span>
        </button>
      </div>
      <!-- JavaScript -->
      <div class="pr-button5 ">
        <button on:click={() => showSection('javascript')} class="mr-10  h-44  w-32 text-slate-200 bg-neutral-800 rounded-xl flex flex-col justify-center shadow duration-300 hover:bg-slate-200 hover:text-neutral-900 hover:shadow-xl">
          <svg xmlns="http://www.w3.org/2000/svg" class="h-14" viewBox="0 0 448 512"><!--! Font Awesome Free 6.4.2 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2023 Fonticons, Inc. --><style>svg{fill:#171717}</style><path d="M0 32v448h448V32H0zm243.8 349.4c0 43.6-25.6 63.5-62.9 63.5-33.7 0-53.2-17.4-63.2-38.5l34.3-20.7c6.6 11.7 12.6 21.6 27.1 21.6 13.8 0 22.6-5.4 22.6-26.5V237.7h42.1v143.7zm99.6 63.5c-39.1 0-64.4-18.6-76.7-43l34.3-19.8c9 14.7 20.8 25.6 41.5 25.6 17.4 0 28.6-8.7 28.6-20.8 0-14.4-11.4-19.5-30.7-28l-10.5-4.5c-30.4-12.9-50.5-29.2-50.5-63.5 0-31.6 24.1-55.6 61.6-55.6 26.8 0 46 9.3 59.8 33.7L368 290c-7.2-12.9-15-18-27.1-18-12.3 0-20.1 7.8-20.1 18 0 12.6 7.8 17.7 25.9 25.6l10.5 4.5c35.8 15.3 55.9 31 55.9 66.2 0 37.8-29.8 58.6-69.7 58.6z"/></svg>
          <span class="mt-6 text-sm ?leading-5 font-semibold text-center">javascript</span>
        </button>
      </div>
      <!-- Other -->
      <div class="pr-button6 ">
        <button on:click={() => showSection('other')} class="h-44 w-32 text-slate-200 bg-neutral-800 rounded-xl flex flex-col justify-center shadow duration-300 hover:bg-slate-200 hover:text-neutral-900 hover:shadow-xl">
          <svg xmlns="http://www.w3.org/2000/svg" class="h-14" viewBox="0 0 640 512"><!--! Font Awesome Free 6.4.2 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2023 Fonticons, Inc. --><style>svg{fill:#171717}</style><path d="M308.5 135.3c7.1-6.3 9.9-16.2 6.2-25c-2.3-5.3-4.8-10.5-7.6-15.5L304 89.4c-3-5-6.3-9.9-9.8-14.6c-5.7-7.6-15.7-10.1-24.7-7.1l-28.2 9.3c-10.7-8.8-23-16-36.2-20.9L199 27.1c-1.9-9.3-9.1-16.7-18.5-17.8C173.9 8.4 167.2 8 160.4 8h-.7c-6.8 0-13.5 .4-20.1 1.2c-9.4 1.1-16.6 8.6-18.5 17.8L115 56.1c-13.3 5-25.5 12.1-36.2 20.9L50.5 67.8c-9-3-19-.5-24.7 7.1c-3.5 4.7-6.8 9.6-9.9 14.6l-3 5.3c-2.8 5-5.3 10.2-7.6 15.6c-3.7 8.7-.9 18.6 6.2 25l22.2 19.8C32.6 161.9 32 168.9 32 176s.6 14.1 1.7 20.9L11.5 216.7c-7.1 6.3-9.9 16.2-6.2 25c2.3 5.3 4.8 10.5 7.6 15.6l3 5.2c3 5.1 6.3 9.9 9.9 14.6c5.7 7.6 15.7 10.1 24.7 7.1l28.2-9.3c10.7 8.8 23 16 36.2 20.9l6.1 29.1c1.9 9.3 9.1 16.7 18.5 17.8c6.7 .8 13.5 1.2 20.4 1.2s13.7-.4 20.4-1.2c9.4-1.1 16.6-8.6 18.5-17.8l6.1-29.1c13.3-5 25.5-12.1 36.2-20.9l28.2 9.3c9 3 19 .5 24.7-7.1c3.5-4.7 6.8-9.5 9.8-14.6l3.1-5.4c2.8-5 5.3-10.2 7.6-15.5c3.7-8.7 .9-18.6-6.2-25l-22.2-19.8c1.1-6.8 1.7-13.8 1.7-20.9s-.6-14.1-1.7-20.9l22.2-19.8zM112 176a48 48 0 1 1 96 0 48 48 0 1 1 -96 0zM504.7 500.5c6.3 7.1 16.2 9.9 25 6.2c5.3-2.3 10.5-4.8 15.5-7.6l5.4-3.1c5-3 9.9-6.3 14.6-9.8c7.6-5.7 10.1-15.7 7.1-24.7l-9.3-28.2c8.8-10.7 16-23 20.9-36.2l29.1-6.1c9.3-1.9 16.7-9.1 17.8-18.5c.8-6.7 1.2-13.5 1.2-20.4s-.4-13.7-1.2-20.4c-1.1-9.4-8.6-16.6-17.8-18.5L583.9 307c-5-13.3-12.1-25.5-20.9-36.2l9.3-28.2c3-9 .5-19-7.1-24.7c-4.7-3.5-9.6-6.8-14.6-9.9l-5.3-3c-5-2.8-10.2-5.3-15.6-7.6c-8.7-3.7-18.6-.9-25 6.2l-19.8 22.2c-6.8-1.1-13.8-1.7-20.9-1.7s-14.1 .6-20.9 1.7l-19.8-22.2c-6.3-7.1-16.2-9.9-25-6.2c-5.3 2.3-10.5 4.8-15.6 7.6l-5.2 3c-5.1 3-9.9 6.3-14.6 9.9c-7.6 5.7-10.1 15.7-7.1 24.7l9.3 28.2c-8.8 10.7-16 23-20.9 36.2L315.1 313c-9.3 1.9-16.7 9.1-17.8 18.5c-.8 6.7-1.2 13.5-1.2 20.4s.4 13.7 1.2 20.4c1.1 9.4 8.6 16.6 17.8 18.5l29.1 6.1c5 13.3 12.1 25.5 20.9 36.2l-9.3 28.2c-3 9-.5 19 7.1 24.7c4.7 3.5 9.5 6.8 14.6 9.8l5.4 3.1c5 2.8 10.2 5.3 15.5 7.6c8.7 3.7 18.6 .9 25-6.2l19.8-22.2c6.8 1.1 13.8 1.7 20.9 1.7s14.1-.6 20.9-1.7l19.8 22.2zM464 304a48 48 0 1 1 0 96 48 48 0 1 1 0-96z"/></svg>
          <span class="mt-6 text-sm ?leading-5 font-semibold text-center">Other</span>
        </button>
      </div>
  </div>

  <div class="flex justify-center  items-center mt-10">
    <div class=" relative flex items-center justify-center">
        
      {#if activeSection === 'csharp'}
        <div class="c-section lg:py-4 bg-neutral-800 rounded-xl h-72 w-9/12"
        in:slide={{duration: 300, delay: 100}} out:slide={{duration: 300, delay: 100}}>
          <div class="p-8 sm:p-16 lg:p-16">
            <h2 class="text-2xl font-bold sm:text-3xl text-slate-200">
              C#
            </h2>
  
            <p class="mt-4 text-slate-300">
              The first language i learned was C#, I was always interested in game development and i wanted to make my own games.
              I knew that in order to learn Game Development i had to learn how to program, so I picked up a ebook on C# and started learning.
              I learned how to use .NET, I have experience with WPF, WinForms, ASP.NET and Blazor.
            </p>
  
            
          </div>
        </div>
      {/if}
      
      
      {#if activeSection === 'unity'}
      <div class=" unity-section lg:py-4 bg-neutral-800 rounded-xl  h-72 w-9/12"
      in:slide={{duration: 300, delay: 100}} out:slide={{duration: 300, delay: 100}}
      >
        <div class="p-8 sm:p-16 lg:p-16">
          <h2 class="text-2xl font-bold sm:text-3xl text-slate-200">
            Unity
          </h2>

          <p class="mt-4 text-slate-300">
            The reason why I started programming was because I wanted to make my own games, my game enigne of choice is Unity.
            I preffer making 2d games because, I think that making pixel art is easier than making 3d models. I have experience in both 2d and 3d game development. 
            <br> <br>
            A few of my games can be found <a class=" underline" href="https://arthurvos.itch.io/">here!</a>
          </p>

          
        </div>
      </div>
    {/if}

    {#if activeSection === 'python'}
      <div class=" python-section lg:py-4 bg-neutral-800 rounded-xl  h-72 w-9/12"
      in:slide={{duration: 300, delay: 100}} out:slide={{duration: 300, delay: 100}}
      >
        <div class="p-8 sm:p-16 lg:p-16">
          <h2 class="text-2xl font-bold sm:text-3xl text-slate-200">
            Python
          </h2>

          <p class="mt-4 text-slate-300">
            Python was the second language I ever learned. A few projects I made with it where things like web scrapers, discord bots and even a console app that could control my smart-lights.
            I also own a few Raspberry PI products that I use for home automation, I use python to control them. 
          </p>

          
        </div>
      </div>
    {/if}

    {#if activeSection === 'php'}
      <div class=" php-section lg:py-4 bg-neutral-800 rounded-xl  h-72 w-9/12"
      in:slide={{duration: 300, delay: 100}} out:slide={{duration: 300, delay: 100}}
      >
        <div class="p-8 sm:p-16 lg:p-16">
          <h2 class="text-2xl font-bold sm:text-3xl text-slate-200">
            PHP
          </h2>

          <p class="mt-4 text-slate-300">
            The reason why I started programming was because I wanted to make my own games, my game enigne of choice is Unity.
            I preffer making 2d games because, I think that making pixel art is easier than making 3d models. I have experience in both 2d and 3d game development. 
          </p>

          
        </div>
      </div>
    {/if}

    {#if activeSection === 'javascript'}
      <div class=" javascript-section lg:py-4 bg-neutral-800 rounded-xl  h-72 w-9/12"
      in:slide={{duration: 300, delay: 100}} out:slide={{duration: 300, delay: 100}}
      >
        <div class="p-8 sm:p-16 lg:p-16">
          <h2 class="text-2xl font-bold sm:text-3xl text-slate-200">
            JavaScript
          </h2>

          <p class="mt-4 text-slate-300">
            The reason why I started programming was because I wanted to make my own games, my game enigne of choice is Unity.
            I preffer making 2d games because, I think that making pixel art is easier than making 3d models. I have experience in both 2d and 3d game development. 
          </p>

          
        </div>
      </div>
    {/if}

    {#if activeSection === 'other'}
      <div class=" other-section lg:py-4 bg-neutral-800 rounded-xl  h-72 w-9/12"
      in:slide={{duration: 300, delay: 100}} out:slide={{duration: 300, delay: 100}}
      >
        <div class="p-8 sm:p-16 lg:p-16">
          <h2 class="text-2xl font-bold sm:text-3xl text-slate-200">
            Other
          </h2>

          <p class="mt-4 text-slate-300">
            The reason why I started programming was because I wanted to make my own games, my game enigne of choice is Unity.
            I preffer making 2d games because, I think that making pixel art is easier than making 3d models. I have experience in both 2d and 3d game development. 
          </p>

          
        </div>
      </div>
    {/if}
      
      
    </div> 
  </div>

<style>
    .pr-button, .pr-button2, .pr-button3, .pr-button4, .pr-button5, .pr-button6 {
    opacity: 0;
    filter: blur(5px);
    transform: translateX(-100%);
    
}

</style>