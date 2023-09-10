<script>
    document.addEventListener('DOMContentLoaded', () => {
  const observer = new IntersectionObserver(entries => {
    entries.forEach((entry) => {
      if (entry.isIntersecting) {
        if(entry.target == document.querySelector(".anim-right") || entry.target == document.querySelector(".anim-right2") || entry.target == document.querySelector(".anim-right3") || entry.target == document.querySelector(".anim-right4") || entry.target == document.querySelector(".anim-left") || entry.target == document.querySelector(".anim-left2") || entry.target == document.querySelector(".anim-left3")){
          entry.target.setAttribute("style", "opacity: 1; filter: blur(0); transform: translateX(0); transition: all 1s;")
        } else if(entry.target == document.querySelector(".timeline-right")){
          entry.target.setAttribute("style", "opacity: 1; filter: blur(0); transform: translateX(0); transition: all 1s; ")
        }else if(entry.target == document.querySelector(".timeline-right2")){
          entry.target.setAttribute("style", "opacity: 1; filter: blur(0); transform: translateX(0); transition: all 1s; transition-delay: 200ms; ")
        }else if(entry.target == document.querySelector(".timeline-right3")){
          entry.target.setAttribute("style", "opacity: 1; filter: blur(0); transform: translateX(0); transition: all 1s; transition-delay: 400ms; ")
        }
        
      } else {
        if(entry.target == document.querySelector(".anim-right") || entry.target == document.querySelector(".anim-right2") || entry.target == document.querySelector(".anim-right3") || entry.target == document.querySelector(".timeline-right") || entry.target == document.querySelector(".timeline-right2") || entry.target == document.querySelector(".timeline-right3")){
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

    const animElements = document.querySelectorAll(".anim-right");
    const animElements3 = document.querySelectorAll(".anim-right2");
    const animElements6 = document.querySelectorAll(".anim-right3");
    const animElements7 = document.querySelectorAll(".anim-right4");
    const animElements2 = document.querySelectorAll(".anim-left");
    const animElements4 = document.querySelectorAll(".anim-left2");
    const animElements5 = document.querySelectorAll(".anim-left3");
    const timelineElements = document.querySelectorAll(".timeline-right");
    const timelineElements2 = document.querySelectorAll(".timeline-right2");
    const timelineElements3 = document.querySelectorAll(".timeline-right3");
    const prButton = document.querySelectorAll(".pr-button");
    const prButton2 = document.querySelectorAll(".pr-button2");
    const prButton3 = document.querySelectorAll(".pr-button3");
    const prButton4 = document.querySelectorAll(".pr-button4");
    const prButton5 = document.querySelectorAll(".pr-button5");
    const prButton6 = document.querySelectorAll(".pr-button6");
    animElements.forEach((el) => observer.observe(el));
    animElements2.forEach((el) => observer.observe(el));
    animElements3.forEach((el) => observer.observe(el));
    animElements4.forEach((el) => observer.observe(el));
    animElements5.forEach((el) => observer.observe(el));
    animElements6.forEach((el) => observer.observe(el));
    animElements7.forEach((el) => observer.observe(el));
    timelineElements.forEach((el) => observer.observe(el));
    timelineElements2.forEach((el) => observer.observe(el));
    timelineElements3.forEach((el) => observer.observe(el));
    prButton.forEach((el) => observer.observe(el));
    prButton2.forEach((el) => observer.observe(el));
    prButton3.forEach((el) => observer.observe(el));
    prButton4.forEach((el) => observer.observe(el));
    prButton5.forEach((el) => observer.observe(el));
    prButton6.forEach((el) => observer.observe(el));
    

});
</script>