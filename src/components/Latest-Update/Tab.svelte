<script lang="ts">
	export let current:string = 'eaNews';
</script>

<button
	class="{current === 'eaNews' ? 'selected' : ''} p-2"
	on:click="{() => current = 'eaNews'}"
>Ea News </button>

<button
	class="{current === 'fifa' ? 'selected' : ''} p-4"
	on:click="{() => current = 'fifa'}"
>FIFA</button>

<button
	class="{current === 'starWars' ? 'selected' : ''} p-4"
	on:click="{() => current = 'starWars'}"
>Star Wars </button>

<button
	class="{current === 'madden' ? 'selected' : ''} p-4"
	on:click="{() => current = 'madden'}"
>Madden </button>
<button
	class="{current === 'apexLegends' ? 'selected' : ''} p-4"
	on:click="{() => current = 'apexLegends'}"
>ApexLegends </button>
<button
	class="{current === 'theSims' ? 'selected' : ''} p-4"
	on:click="{() => current = 'theSims'}"
>theSims </button>

<button
	class="{current === 'f1' ? 'selected' : ''} p-4"
	on:click="{() => current = 'f1'}"
>F1</button>

<style>
	.button {
		display: block;
		margin-left: 8rem;
	}

  .selected {
		border-bottom-color: #ff3e00;
		color: #ff3e00;
	}
</style>