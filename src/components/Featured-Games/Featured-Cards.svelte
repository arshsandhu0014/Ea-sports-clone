<!-- Card.svelte -->
<script lang="ts">
	import type { ImportGlobEagerFunction } from "vite";


    // export let title:string;
    // export let content:string;
    export let imageSrc:string;

  </script>
  
  <div class="bg-white flex  shadow-md rounded-md m-4">
    <img src={imageSrc} alt=""> 
    <!-- <h2 class="text-xl font-bold ">{title}</h2>
    <p class="mt-2">{content}</p> -->
  </div>
  