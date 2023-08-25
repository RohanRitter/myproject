<script>
	let firstName = "Rohan";
	let lastName = "Ritter";
	let beltcoulor = "red";

	const handleClick = () => {
		beltcoulor = "black";
	}; 

	const handleInput = (e) => {
		beltcoulor = e.target.value;
	}; 
</script>

<main>
	<h1>Hello {firstName} {lastName}!</h1>
	<p style="color: {beltcoulor};">Our best {beltcoulor} belt user!</p>
	<button on:click={handleClick}>Update belt colour</button>
	<!-- <input type="text" on:input={handleInput}> (One way binding)--> 
	<input type="text" bind:value={beltcoulor}> <!-- (Two way binding) -->
</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: #ff3e00;
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