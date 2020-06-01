<script>
	import Navbar from "./Navbar.svelte";
	import Player from "./Player.svelte";
	import AddPlayer from "./AddPlayer.svelte";
	let players = [{
			name: "Abdelrhman",
			points: 100
		},
		{
			name: "Tarek",
			points: 90
		},
		{
			name: "Wahba",
			points: 80
		}
	]

	const addplayer = (e) => {
		players = [...players, e.detail];
	}
	const deleteplayer = (e) => {
		players = players.filter((player) => player.name != e.detail)
	}
</script>

<Navbar />
<AddPlayer on:addplayer={addplayer} />
<div class="container">
	{#if (players.length ===0)}
	NO PLAYERS
	{:else}
	{#each players as player}
	<Player name= {player.name} points={player.points} on:deleteplayer={deleteplayer}/>
	{/each}
	{/if}
</div>