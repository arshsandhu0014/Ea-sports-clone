<!-- Card.svelte -->
<script lang="ts">

    export let title:string;
    export let content:string;

  </script>
  
  <div class="bg-white shadow-md rounded-md p-6">
    <h2 class="text-xl font-bold">{title}</h2>
    <p class="mt-2">{content}</p>
  </div>
  