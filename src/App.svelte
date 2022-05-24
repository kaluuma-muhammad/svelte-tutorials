<script>
	let firstName = "Meddy";
	let lastName = "Clays";
	let color = "Black";

	// Reative value
	$: fullName = `${firstName} ${lastName}`;

	// const changeColor = () => {
	// 	color = "Red";
	// };

	// const inputChangeColor = (e) => {
	// 	color = e.target.value;
	// };
</script>

<main>
	<p>Name: {fullName} - Favourite color: {color}</p>

	<input type="text" placeholder="First Name" bind:value={firstName}>
	<input type="text" placeholder="Last Name" bind:value={lastName}>
	<input type="text" placeholder="Enter Color" bind:value={color}>
</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	/* h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	} */

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>