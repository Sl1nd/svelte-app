<script>
	let name = 'world';
	let characters =  [];

	let test = () => fetch('https://rickandmortyapi.com/api/character/').then(response => response.json())
  			.then(data => {
			characters = data.results
			});
</script>

<h1>Hello {name}!</h1>
<button on:click={test}>click me</button>
<ul>
	{#each characters as character}
		<li>{character.name}</li>
	{/each}
</ul>