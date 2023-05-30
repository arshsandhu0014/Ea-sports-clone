
<script lang="ts">
	import Tab from "./Tab.svelte";
	import LatestUpdateCard from "./LatestUpdateCard.svelte";
	import { current_component } from "svelte/internal";
  export let current_value:string="eaNews";

    let eaNews_cards_data = [
  { title: 'Card 1', content: 'Content for Card 1' , imageSrc:'./images/LatestUpdate/cards/eaNews/1.jpg', },
  { title: 'Card 2', content: 'Content for Card 2', imageSrc:'./images/LatestUpdate/cards/eaNews/2.jpg' },
  { title: 'Card 3', content: 'Content for Card 3', imageSrc:'./images/LatestUpdate/cards/eaNews/3.jpg' },
  { title: 'Card 4', content: 'Content for Card 3', imageSrc:'./images/LatestUpdate/cards/eaNews/4.jpg' },
  { title: 'Card 5', content: 'Content for Card 3', imageSrc:'./images/LatestUpdate/cards/eaNews/5.jpg' },
  { title: 'Card 6', content: 'Content for Card 3', imageSrc:'./images/LatestUpdate/cards/eaNews/6.jpg' },
];
let fifa_cards_data = [
  { title: 'Card 7', content: 'Content for Card 1' , imageSrc:'./images/LatestUpdate/cards/fifa/1.jpg', },
  { title: 'Card 8', content: 'Content for Card 2', imageSrc:'./images/LatestUpdate/cards/fifa/2.jpg' },
  { title: 'Card 9', content: 'Content for Card 3', imageSrc:'./images/LatestUpdate/cards/fifa/3.jpg' },
  { title: 'Card 10', content: 'Content for Card 3', imageSrc:'./images/LatestUpdate/cards/fifa/4.png' },
  { title: 'Card 11', content: 'Content for Card 3', imageSrc:'./images/LatestUpdate/cards/fifa/5.jpg' },
  { title: 'Card 12', content: 'Content for Card 3', imageSrc:'./images/LatestUpdate/cards/fifa/6.jpg' },
];

let starWars_cards_data = [
  { title: 'Card 13', content: 'Content for Card 1' , imageSrc:'./images/LatestUpdate/cards/Starwars/1.png', },
  { title: 'Card 14', content: 'Content for Card 2', imageSrc:'./images/LatestUpdate/cards/Starwars/2.jpg' },
  { title: 'Card 15', content: 'Content for Card 3', imageSrc:'./images/LatestUpdate/cards/Starwars/3.jpg' },
  { title: 'Card 16', content: 'Content for Card 3', imageSrc:'./images/LatestUpdate/cards/Starwars/4.jpg' },
  { title: 'Card 17', content: 'Content for Card 3', imageSrc:'./images/LatestUpdate/cards/Starwars/5.jpg' },
  { title: 'Card 18', content: 'Content for Card 3', imageSrc:'./images/LatestUpdate/cards/Starwars/6.jpg' },
];
let madden_cards_data = [
  { title: 'Card 1', content: 'Content for Card 1' , imageSrc:'./images/LatestUpdate/cards/Madden/1.jpg', },
  { title: 'Card 2', content: 'Content for Card 2', imageSrc:'./images/LatestUpdate/cards/Madden/2.jpg' },
  { title: 'Card 3', content: 'Content for Card 3', imageSrc:'./images/LatestUpdate/cards/Madden/3.jpg' },
  { title: 'Card 3', content: 'Content for Card 3', imageSrc:'./images/LatestUpdate/cards/Madden/4.jpg' },
  { title: 'Card 3', content: 'Content for Card 3', imageSrc:'./images/LatestUpdate/cards/Madden/5.jpg' },
  { title: 'Card 3', content: 'Content for Card 3', imageSrc:'./images/LatestUpdate/cards/Madden/6.jpg' },
];
let apexLegends_cards_data = [
  { title: 'Card 1', content: 'Content for Card 1' , imageSrc:'./images/LatestUpdate/cards/ApexLegends/1.jpg', },
  { title: 'Card 2', content: 'Content for Card 2', imageSrc:'./images/LatestUpdate/cards/ApexLegends/2.jpg' },
  { title: 'Card 3', content: 'Content for Card 3', imageSrc:'./images/LatestUpdate/cards/ApexLegends/3.png' },
  { title: 'Card 3', content: 'Content for Card 3', imageSrc:'./images/LatestUpdate/cards/ApexLegends/4.jpg' },
  { title: 'Card 3', content: 'Content for Card 3', imageSrc:'./images/LatestUpdate/cards/ApexLegends/5.jpg' },
  { title: 'Card 3', content: 'Content for Card 3', imageSrc:'./images/LatestUpdate/cards/ApexLegends/6.png' },
];
let theSims_cards_data = [
  { title: 'Card 1', content: 'Content for Card 1' , imageSrc:'./images/LatestUpdate/cards/Thesims/1.png', },
  { title: 'Card 2', content: 'Content for Card 2', imageSrc:'./images/LatestUpdate/cards/Thesims/2.jpg' },
  { title: 'Card 3', content: 'Content for Card 3', imageSrc:'./images/LatestUpdate/cards/Thesims/3.jpg' },
  { title: 'Card 3', content: 'Content for Card 3', imageSrc:'./images/LatestUpdate/cards/Thesims/4.png' },
  { title: 'Card 3', content: 'Content for Card 3', imageSrc:'./images/LatestUpdate/cards/Thesims/5.png' },
  { title: 'Card 3', content: 'Content for Card 3', imageSrc:'./images/LatestUpdate/cards/Thesims/6.jpg' },
];
let f1_cards_data = [
  { title: 'Card 1', content: 'Content for Card 1' , imageSrc:'./images/LatestUpdate/cards/f1/1.jpg', },
  { title: 'Card 2', content: 'Content for Card 2', imageSrc:'./images/LatestUpdate/cards/f1/2.jpg' },
  { title: 'Card 3', content: 'Content for Card 3', imageSrc:'./images/LatestUpdate/cards/f1/3.jpg' },
  { title: 'Card 3', content: 'Content for Card 3', imageSrc:'./images/LatestUpdate/cards/f1/4.jpg' },
  { title: 'Card 3', content: 'Content for Card 3', imageSrc:'./images/LatestUpdate/cards/f1/5.jpg' },
  { title: 'Card 3', content: 'Content for Card 3', imageSrc:'./images/LatestUpdate/cards/f1/6.jpg' },
];
    

  </script>


<div class="container">
    <h1 class="  flex justify-center text-6xl mb-20">Latest Updates</h1>


    <div class="flex justify-center text-2xl pb-4">
      <Tab bind:current={current_value}/>
    </div>
 
    <div class=" flex justify-center  ">

      <div class="flex justify-center">
        <div class="bg-white shadow-md rounded-md ml-44 mr-44">
       <div class="grid grid-cols-3 gap-4">
        {#if (current_value =="eaNews")}
         {#each eaNews_cards_data as eaNews, i}
           <LatestUpdateCard imageSrc={eaNews.imageSrc} content={eaNews.content} title={eaNews.title}/>
   
         {/each}
         {:else if (current_value =="fifa") }
         {#each fifa_cards_data as fifa, i}
         <LatestUpdateCard imageSrc={fifa.imageSrc} content={fifa.content} title={fifa.title}/>
 
         {/each}

         {:else if (current_value =="starWars") }

         {#each starWars_cards_data as starWars, i}
         <LatestUpdateCard imageSrc={starWars.imageSrc} content={starWars.content} title={starWars.title}/>
 
         {/each}

         {:else if (current_value =="madden") }

         {#each madden_cards_data as madden, i}
         <LatestUpdateCard imageSrc={madden.imageSrc} content={madden.content} title={madden.title}/>
 
         {/each}
         {:else if (current_value =="apexLegends") }

         {#each apexLegends_cards_data as apexLegends, i}
         <LatestUpdateCard imageSrc={apexLegends.imageSrc} content={apexLegends.content} title={apexLegends.title}/>
 
         {/each}
         {:else if (current_value =="theSims") }

         {#each theSims_cards_data as theSims, i}
         <LatestUpdateCard imageSrc={theSims.imageSrc} content={theSims.content} title={theSims.title}/>
 
         {/each}
         {:else if (current_value =="f1") }

         {#each f1_cards_data as f1, i}
         <LatestUpdateCard imageSrc={f1.imageSrc} content={f1.content} title={f1.title}/>
 
         {/each}


         {/if}
       </div>
     </div>
     
     <div>
    </div>
    </div>
   
    </div>
    
    
</div>

  