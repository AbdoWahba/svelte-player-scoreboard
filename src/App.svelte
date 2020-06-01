<script>
	import Navbar from "./Navbar.svelte"
	let name = "Abdelrhman tarek";
	let points = 100;
	let showControlers = false;
	const addPoint = () => {
		points += 1
	}
	const removePoint = () => {
		points -= 1
	}
	const toggleControlers = () => {
		showControlers = !showControlers
	}
</script>

<style>
	.u-m-b-5 {
		margin-bottom: 50px;
	}
</style>

<Navbar />
<div class="container">
	<div class="card">
		<h1>{name}</h1>
		<h3>{points}</h3>
		<button class="btn btn-sm btn-secondary u-m-b-5" on:click={toggleControlers}>
			{#if (showControlers)} + {:else} - {/if}
		</button>
		{#if (showControlers)}
		<button class="btn" on:click={addPoint}>+1</button>
		<button class="btn btn-dark" on:click={removePoint}>-1</button>
		<input type="number" bind:value={points}>
		{/if}
	</div>
</div>