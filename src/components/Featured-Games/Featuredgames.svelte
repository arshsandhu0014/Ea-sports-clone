<script lang="ts">
  
   
import Cards from "./Featured-Cards.svelte";

    let cards = [
  { title: 'Card 1', content: 'Content for Card 1' , imageSrc:'./images/Featured-games/star-wars-.jpg', },
  { title: 'Card 2', content: 'Content for Card 2', imageSrc:'./images/Featured-games/ea-sports.jpg' },
  { title: 'Card 3', content: 'Content for Card 3', imageSrc:'./images/Featured-games/the-sims.jpg' },
  { title: 'Card 3', content: 'Content for Card 3', imageSrc:'./images/Featured-games/eas-fifa.jpg' },
  { title: 'Card 3', content: 'Content for Card 3', imageSrc:'./images/Featured-games/madden-23.jpg' },
  { title: 'Card 3', content: 'Content for Card 3', imageSrc:'./images/Featured-games/apex-legends.jpg' },
];
 
</script>

<div class="container mt-[600px] max-w-full">
    <h1 class="  flex justify-center text-5xl pt ">Featured Games</h1>
  </div>

     <div class="flex justify-center">
     <div class="bg-white shadow-md rounded-md ml-44 mr-44">
    <div class="grid grid-cols-3 gap-4">
      {#each cards as card, i}
        <Cards imageSrc={card.imageSrc} />

      {/each}
    </div>
  </div>
  <div>
    <button> </button>
  </div>

</div>

<div class="flex justify-center mt-10">

    <button class=" flex items-center text-black   button-border text-2xl ml-5 mt-2 mb-20 pr-10 pl-10 pt-5 pb-5 rounded"> Latest Games</button>
</div>


      <style>

.button-border{
         
         border-style: solid;
         border-color: rgb(0, 0, 0);
         border-width: 2px;
     }
      </style>

    


    



    
  
  