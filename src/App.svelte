<script>
	import Navbar from "./Navbar.svelte";
	import Player from "./Player.svelte";
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
</script>


<Navbar />
<div class="container">
	{#each players as player}
	<Player name= {player.name} points={player.points}/>
	{/each}
</div>