<script>
	let name = "Abdelrhman tarek";
	let points = 100;
	const addPoint = () => {
		points += 1
	}
	const removePoint = () => {
		points -= 1
	}
</script>

<style>

</style>

<div class="container">
	<div class="card">
		<h1>{name}</h1>
		<h3>{points}</h3>
		<button class="btn" on:click={addPoint}>+1</button>
		<button class="btn btn-dark" on:click={removePoint}>-1</button>
		<input type="number" bind:value={points}>
	</div>
</div>