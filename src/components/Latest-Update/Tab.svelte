<script lang="ts">
	export let current:string = 'eaNews';
</script>


<div class="flex justify-start">
	
	<button
	class="{current === 'eaNews' ? 'selected' : ''} select p-1 sm:p-2"
	on:click="{() => current = 'eaNews'}"
	>Ea News </button>

	<button
	class="{current === 'fifa' ? 'selected' : ''} select p-1 sm:p-4"
	on:click="{() => current = 'fifa'}"
>FIFA</button>

<button
class="{current === 'starWars' ? 'selected' : ''} select p-1 sm:p-4"
on:click="{() => current = 'starWars'}"
>Star Wars </button>

<button
class="{current === 'madden' ? 'selected' : ''} select p-1 sm:p-4"
on:click="{() => current = 'madden'}"
>Madden </button>
<button
class="{current === 'apexLegends' ? 'selected' : ''}  select p-1 sm:p-4"
on:click="{() => current = 'apexLegends'}"
>ApexLegends </button>
<button
class="{current === 'theSims' ? 'selected' : ''} select  p-1 sm:p-4"
on:click="{() => current = 'theSims'}"
>theSims </button>

<button
class="{current === 'f1' ? 'selected' : ''} select p-1 sm:p-4"
	on:click="{() => current = 'f1'}"
>F1</button>

</div>


<style>
	/* .button {
		display: block;
		margin-left: 8rem;
	} */
	
	.selected {
		
		
		color: #373231;
		background-color: #f3f3f3;
		border-bottom-color: #ff3e00;
		border-width: 2px;
		
	}
	.select:hover {
		
		
		color: #373231;
		background-color: #f3f3f3;
	
		
	}

	
</style>