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

<div class="relative sm:w-auto flex shadow-2xl rounded-md">
  <!-- Logo -->
  <div class="z-[1] logo flex justify-center items-center w-[100%] h-[100%] bg-grad">
    <img class="h-[10rem] w-[10rem] slide-top" src={imageSrcLogo} alt="/" />
  </div>

  <!-- Background Image -->
  <div class="eapl-game-box__background-link">
    <img class="" src={imageSrc} alt="/" />
  </div>
</div>

<style>
  /* Gradient background on hover */
  .bg-grad:hover {
    background: rgb(0, 0, 0);
    background: linear-gradient(
      90deg,
      rgba(0, 0, 0, 0.8324579831932774) 0%,
      rgba(215, 20, 20, 0.8380602240896359) 100%
    );
  }

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
      transform: translateY(-100px);
    }
  }

  /* Apply slide animation on hover */
  .slide-top:hover {
    animation: slide-top 0.5s ease-out both;
  }
</style>