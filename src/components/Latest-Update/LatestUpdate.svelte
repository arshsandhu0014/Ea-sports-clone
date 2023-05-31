
<script lang="ts">
	import Tab from "./Tab.svelte";
	import LatestUpdateCard from "./LatestUpdateCard.svelte";
	import { current_component } from "svelte/internal";
  export let current_value:string="eaNews";
  import {eaNews_cards_data} from "./data";
  import {fifa_cards_data} from "./data";
  import {apexLegends_cards_data} from "./data";
  import {madden_cards_data} from "./data";
  import {theSims_cards_data} from "./data";
  import {starWars_cards_data} from "./data";
  import {f1_cards_data} from "./data";


  </script>


<div class=" w-[100vw]">
    <h1 class="  flex justify-center text-3xl md:text-6xl mb-20">Latest Updates</h1>


    <div class="flex justify-center  text-base sm:text-lg md:text-2xl pb-4">
      <Tab bind:current={current_value}/>
    </div>
 
    <div class=" flex justify-center  ">

      <div class="flex justify-center">
        <div class="bg-white flex justify-self-center shadow-md rounded-md ">
       <div class=" grid grid-cols-1 sm:grid-cols-2  md:grid-cols-3 gap-4 ">
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

  