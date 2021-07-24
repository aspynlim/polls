<script>
	let firstName = 'James';
	let lastName = 'Kim';
	let color = 'red';

	$: fullName = `${firstName} ${lastName}`;
	$: console.log(color);
</script>

<main>
	<p>{fullName}</p>
	<input type="text" bind:value={firstName}/>
	<input type="text" bind:value={lastName}/>
	<input type="text" bind:value={color}>
</main>

<style lang="scss">
	@import "./styles/styles.scss";

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