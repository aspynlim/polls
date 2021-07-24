<script>
	let people = [
		// {name: 'jen', color:'red', age: 20, id: 1},
		// {name: 'kyle', color:'black', age: 30, id: 2},
		// {name: 'sam', color:'purple', age: 40, id: 3},
	]
</script>

<main>
	{#each people as person (person.id)}
		<div>
			<h4>{person.name}</h4>
			<p>{person.age}</p>
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