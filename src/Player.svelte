<script>
    export let name;
    export let points;
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

</style>


<div class="card">
    <h1>{name}</h1>
    <h3>{points}</h3>
</div>
<button class="btn btn-sm btn-secondary " on:click={toggleControlers}>
    {#if (showControlers)} - {:else} + {/if}
		</button>
		{#if (showControlers)}
			<button type="button" class="btn btn-dark" on:click={removePoint}>-1</button>
			<button type="button" class="btn" on:click={addPoint}>+1</button>
			<input type="number" bind:value={points}>
		{/if}