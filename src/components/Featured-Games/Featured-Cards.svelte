<!-- Card.svelte -->
<script lang="ts">
  import type { ImportGlobEagerFunction } from "vite";

  // Exported props
  // export let title: string;
  // export let content: string;
  export let imageSrc: string;
  export let imageSrcLogo: string;

  console.log(imageSrcLogo);
  console.log(imageSrc);
</script>

<div class="relative sm:w-auto flex shadow-2xl parent rounded-md">
  <!-- Logo -->
  <div class="z-[1] logo flex justify-center items-center w-[100%] h-[100%] scale-up-top fade-in-fwd bg-grad ">
    <img class="h-[10rem] w-[10rem] slide-top" src={imageSrcLogo} alt="/" />
  </div>

  <!-- Background Image -->
  <div class="eapl-game-box__background-link">
    <img class="" src={imageSrc} alt="/" />
  </div>
</div>

<style>
  /* Gradient background on hover */
  /* .bg-grad:hover {
    background: rgb(22,1,73);
    background: linear-gradient(90deg, rgba(22,1,73,0.8324579831932774) 0%, rgba(238,32,32,0.8380602240896359) 100%);
  } */

  /* Logo styles */
  .logo {
    position: absolute;
    top: 0;
    bottom: 0;
    left: 0;
    right: 0;
    justify-content: center;
    z-index: 1;
  }

 


  /* .parent:hover .scale-up-top {
    background: rgb(22,1,73);
    background: linear-gradient(90deg, rgba(22,1,73,0.8324579831932774) 0%, rgba(238,32,32,0.8380602240896359) 100%);
	-webkit-animation: scale-up-top 0.4s cubic-bezier(0.390, 0.575, 0.565, 1.000) both;
	        animation: scale-up-top 0.4s cubic-bezier(0.390, 0.575, 0.565, 1.000) both;
} */
  

  /* Background image container styles */
  .eapl-game-box__background-link {
    position: relative;
    z-index: 0;
    height: inherit;
    width: inherit;
  }

  /* Slide animation */
  @keyframes slide-top {
    0% {
      transform: translateY(0);
    }
    100% {
      transform: translateY(-60px);
    }
  }

  /* Apply slide animation on hover */
  .parent:hover .slide-top {
    animation: slide-top 0.5s ease-out both;
  }

/* ----------------------------------------------
 * Generated by Animista on 2023-6-2 16:31:49
 * Licensed under FreeBSD License.
 * See http://animista.net/license for more info. 
 * w: http://animista.net, t: @cssanimista
 * ---------------------------------------------- */

/**
 * ----------------------------------------
 * animation scale-up-top
 * ----------------------------------------
 */
 @-webkit-keyframes scale-up-top {
  0% {
    -webkit-transform: scale(0.5);
            transform: scale(0.5);
    -webkit-transform-origin: 50% 0%;
            transform-origin: 50% 0%;
  }
  100% {
    -webkit-transform: scale(1);
            transform: scale(1);
    -webkit-transform-origin: 50% 0%;
            transform-origin: 50% 0%;
  }
}
@keyframes scale-up-top {
  0% {
    -webkit-transform: scale(0.5);
            transform: scale(0.5);
    -webkit-transform-origin: 25% 0%;
            transform-origin: 25% 0%;
  }
  100% {
    -webkit-transform: scale(1);
            transform: scale(1);
    -webkit-transform-origin: 50% 0%;
            transform-origin: 50% 0%;
  }
}


  /* .scale-up-top:hover {
    background: rgb(22,1,73);
    background: linear-gradient(90deg, rgba(22,1,73,0.8324579831932774) 0%, rgba(238,32,32,0.8380602240896359) 100%);
	-webkit-animation: scale-up-top 0.4s cubic-bezier(0.390, 0.575, 0.565, 1.000) both;
	        animation: scale-up-top 0.4s cubic-bezier(0.390, 0.575, 0.565, 1.000) both;
} */
/* ----------------------------------------------
 * Generated by Animista on 2023-6-2 16:53:21
 * Licensed under FreeBSD License.
 * See http://animista.net/license for more info. 
 * w: http://animista.net, t: @cssanimista
 * ---------------------------------------------- */

/**
 * ----------------------------------------
 * animation fade-in-fwd
 * ----------------------------------------
 */
 @-webkit-keyframes fade-in-fwd {
  0% {
    -webkit-transform: translateZ(-80px);
            transform: translateZ(-80px);
    opacity: 0;
  }
  100% {
    -webkit-transform: translateZ(0);
            transform: translateZ(0);
    opacity: 1;
  }
}
@keyframes fade-in-fwd {
  0% {
    -webkit-transform: translateZ(-80px);
            transform: translateZ(-80px);
    opacity: 0;
  }
  100% {
    -webkit-transform: translateZ(0);
            transform: translateZ(0);
    opacity: 1;
  }
}

.parent:hover .fade-in-fwd {
  background: rgb(22,1,73);
background: linear-gradient(90deg, rgba(22,1,73,0.8324579831932774) 0%, rgba(252,74,74,0.8380602240896359) 100%);
	-webkit-animation: fade-in-fwd 0.6s cubic-bezier(0.390, 0.575, 0.565, 1.000) both;
	        animation: fade-in-fwd 0.6s cubic-bezier(0.390, 0.575, 0.565, 1.000) both;
}

</style>