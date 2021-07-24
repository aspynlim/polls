<script>
	let name = 'James';
	let color = 'green';

	const handleClick = () => {
		color = 'red';
	};

	const handleInput = (e) => {
		color = e.target.value;
	};
</script>

<main>
	<h1>Hello {name}!</h1>
	<p style="color: {color}">{color}</p>
	<button on:click={handleClick}>UPDATE</button>
	<!-- <input type="text" on:input={handleInput} value={color}/> -->
	<input type="text" bind:value={color}>
</main>

<style lang="scss">
	@import "./styles/variables.scss";

	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: $blue;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>