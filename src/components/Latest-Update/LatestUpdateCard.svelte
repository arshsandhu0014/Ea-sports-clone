<script lang="ts">
	import type { ImportGlobEagerFunction } from "vite";


    export let title:string;
    export let content:string;
    export let imageSrc:string;


  </script>
  
  <div class="bg-white flex flex-col  shadow-md rounded-md m-4">
    <img src={imageSrc} alt="" height="300px" width="300px"> 
    <h2 class="text-xl font-bold text-center ">{title}</h2>
    <p class="mt-2 text-center">{content}</p>
  </div>
  