<script>
    let name;
    let favColor;
    let age;
	let skills = [];

	const handleSubmit = () => {
		console.log(name, favColor, age, skills);
	};
</script>

<main>
    <h3>Add New Person</h3>
	<form on:submit|preventDefault={handleSubmit}>
		<div class="">
			<input type="text" name="name" bind:value={name} placeholder="Enter Name">
		</div>
		
		<div class="">
			<input type="number" name="age" bind:value={age} placeholder="Enter Age">
		</div>
		
		<div class="">
			<label for="skills">Skills</label>
			<input type="checkbox" bind:group={skills} value="fighting">Fighting<br>
			<input type="checkbox" bind:group={skills} value="sneaking">Sneaking<br>
			<input type="checkbox" bind:group={skills} value="running">Running
		</div>

		<div class="">
			<label for="favColor">Favourite Color</label>
			<select bind:value={favColor}>
				<option value="Green">Green</option>
				<option value="Blue">Blue</option>
				<option value="Black">Black</option>
			</select>
		</div>
		<button>Add Person</button>
	</form>
</main>

<style>
    /* your styles go here */
</style>