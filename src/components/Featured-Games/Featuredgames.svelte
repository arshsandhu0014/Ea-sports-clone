<script lang="ts">
  
   
import Cards from "../Featured-Games/Cards.svelte";

    let cards = [
  { title: 'Card 1', content: 'Content for Card 1' },
  { title: 'Card 2', content: 'Content for Card 2' },
  { title: 'Card 3', content: 'Content for Card 3' },
];
 
</script>

<div class="container mt-[600px] max-w-full">
    <h1 class="  flex justify-center text-5xl pb-10 pt-20 ">Featured Games</h1>
</div>

     <div class=" flex justify-center">  
    <div class="bg-white shadow-md rounded-md p-6">
        <div class="bg-white shadow-md rounded-md p-6">
            <div>
                {#each cards as card}
                  <Cards title= {card.title} content={card.content} />
                {/each}
              </div>
              
            </div>
      </div>

     </div>

    


    



    
  
  