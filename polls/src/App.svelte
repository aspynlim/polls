<script>
	let people = [
		{name: 'jen', color:'red', age: 20, id: 1},
		{name: 'kyle', color:'black', age: 30, id: 2},
		{name: 'sam', color:'purple', age: 40, id: 3},
	];

	const handleClick = (e, id) => {
		people = people.filter((person) => person.id != id);
		console.log(e);
	};

	let num = 5;
</script>

{#if num > 20}
	<p>Graeter than 20</p>
{:else if num > 5}
	<p>Greater than 5</p>
{:else}
	<p>Default</p>
{/if}

<main>
	{#each people as person (person.id)}
		<div>
			{#if person.color === 'red'}
				<p><strong>RESULT : {person.color}</strong></p>
			{/if}
			<h4>{person.name}</h4>
			<p>{person.age}</p>
			<button on:click={(e) => handleClick(e, person.id)}>DELETE</button>
		</div>
	{:else}
		<p>There's no one to show.</p>
	{/each}
</main>

<style lang="scss">
	@import "./styles/styles.scss";

	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>