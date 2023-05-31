<!-- Card.svelte -->
<script lang="ts">
	import type { ImportGlobEagerFunction } from "vite";


    // export let title:string;
    // export let content:string;
    export let imageSrc:string;

  </script>
  
  <div class="bg-white w-[100%] sm:w-auto flex shadow-md rounded-md ">
    <img src={imageSrc} alt=""> 
    <!-- <h2 class="text-xl font-bold ">{title}</h2>
    <p class="mt-2">{content}</p> -->
  </div>
  