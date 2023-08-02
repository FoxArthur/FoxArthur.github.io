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

  const observer = new IntersectionObserver(entries => {
    entries.forEach(entry => {
      const id = entry.target.getAttribute("id");
      if (entry.intersectionRatio > 0) {
        entry.target.classList.add("active");
      } else {
        entry.target.classList.remove("active");
      }
    });
  });

  const animElements = document.querySelectorAll(".anim");
  animElements.forEach(el => {
    observer.observe(el);
  });

</script>
<main>
    <div id="fullpage">
      <div class="section bg-neutral-950">
        <div class="grid sm:grid-cols-2 ">
          <div class="flex items-center justify-center h-screen">
            <h1 class=" title text-white text-center text-8xl">Arthur Vos</h1>
          </div>
          <div>
            
          </div>
        </div>
      </div>
      <div class="section">
        <h1 class=" text-xl">dwddwdw</h1>   
      </div>
      <div class="section">Some section</div>
      <div class="section">Some section</div>
  </div>
</main>
<style>
  h1{
    font-family: league;
  }

  .title {
  box-shadow: inset 0 0 0 0 black;
  color: white;
  margin: 0 -.1rem;
  padding: 0 .1rem;
  padding-top: 1rem;  
  transition: color .6s ease-in-out, box-shadow .5s ease-in-out;
}
.title:hover {
  box-shadow: inset 1000px 0 0 0 white;
  color: black;
}
</style>
