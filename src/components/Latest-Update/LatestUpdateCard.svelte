<script lang="ts">
	import type { ImportGlobEagerFunction } from "vite";


    export let title:string;
    export let content:string;
    export let imageSrc:string;


  </script>
  
  <div class="bg-white  max-h-[30rem] lg:w-[18rem] flex flex-col w- hover:shadow-2xl hover:-translate-y-1 hover:scale-105 transition duration-300 ease-in-out shadow-md rounded-md m-4">
    <img src={imageSrc} alt="/"> 
    <h2 class=" md:text-lg font-bold ml-2 mr-2 mt-5 ">{title}</h2>
    <p class="mt-2 md:text-lg p-2 text-sm">{content}</p>
  </div>
  
  <style>


  </style>