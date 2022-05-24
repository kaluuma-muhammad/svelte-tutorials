<script>
	let name = "Meddy";
	let country = "Uganda";
	let district = "Kampala";
	let color = "Black";

	const changeDistrict = () => {
		district = "Mpigi";
	};

	const changeColor = () => {
		color = "Red";
	};

	// const inputChangeColor = (e) => {
	// 	color = e.target.value;
	// };
</script>

<main>
	<h1>Hello {name}!</h1>
	<p>From: {country}</p>
	<p>District: {district}</p>
	<p style="color: {color};">Favourite color: {color}</p>

	<button on:click={changeDistrict}>Change District</button><br>
	<button on:click={changeColor}>Change Fovourite Color</button>

	<!-- <input type="text" on:input={inputChangeColor} value={color}> -->
	<input type="text" placeholder="Enter Color" bind:value={color}>
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