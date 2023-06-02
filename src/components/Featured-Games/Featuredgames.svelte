<script lang="ts">
  import Cards from "./Featured-Cards.svelte";

  // Array of card data
  let cards = [
    {
      title: 'Card 1',
      content: 'Content for Card 1',
      imageSrc: './images/Featured-games/star-wars-.jpg',
      imageSrcLogo: '/images/Featured-games/logo/star-wars.svg'
    },
    {
      title: 'Card 2',
      content: 'Content for Card 2',
      imageSrc: './images/Featured-games/ea-sports.jpg',
      imageSrcLogo: '/images/Featured-games/logo/pga.svg'
    },
    {
      title: 'Card 3',
      content: 'Content for Card 3',
      imageSrc: './images/Featured-games/the-sims.jpg',
      imageSrcLogo: '/images/Featured-games/logo/thesims.svg'
    },
    {
      title: 'Card 4',
      content: 'Content for Card 4',
      imageSrc: './images/Featured-games/eas-fifa.jpg',
      imageSrcLogo: '/images/Featured-games/logo/fifa23.svg'
    },
    {
      title: 'Card 5',
      content: 'Content for Card 5',
      imageSrc: './images/Featured-games/madden-23.jpg',
      imageSrcLogo: '/images/Featured-games/logo/m23.svg'
    },
    {
      title: 'Card 6',
      content: 'Content for Card 6',
      imageSrc: './images/Featured-games/apex-legends.jpg',
      imageSrcLogo: '/images/Featured-games/logo/apex-legends.svg'
    },
  ];
</script>

<!-- Container -->
<div class="container w-[100]">
  <h1 class="flex justify-center text-4xl pt-14 pb-20">Featured Games</h1>
</div>

<!-- Cards Section -->
<div class="flex justify-center">
  <div class="bg-white shadow-md rounded-md mr-2 ml-2 sm:ml-44 sm:mr-44">
    <div class="grid grid-cols-1 md:grid-cols-3 gap-4">
      {#each cards as card, i}
        <Cards imageSrc={card.imageSrc} imageSrcLogo={card.imageSrcLogo} />
      {/each}
    </div>
  </div>
  <div>
    <button></button>
  </div>
</div>

<!-- Latest Games Button -->
<div class="flex justify-center">
  <button class="flex items-center text-black button-border text-2xl ml-5 mt-10 mb-20 pr-10 pl-10 pt-5 pb-5 rounded hover:-translate-y-1 hover:scale-105 transition duration-300 ease-in-out">
    Latest Games
  </button>
</div>

<style>
  .button-border {
    border-style: solid;
    border-color: rgb(0, 0, 0);
    border-width: 2px;
  }
</style>