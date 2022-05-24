<script>
	let people = [
		{id: 1, name: 'Shakira', age: 17, favColor: 'Red'},
		{id: 2, name: 'Roman', age: 20, favColor: 'Blue'},
		{id: 3, name: 'Malone', age: 23, favColor: 'Black'}
	];

	const deletePerson = (id) => {
		// Delete person
		people = people.filter((person) => person.id != id);
	};
</script>

<main>
	{#each people as person (person.id)}
		<div>
			<h3>{person.name} <samp><i>{person.age}yrs</i></samp></h3>
			<p>Favourite colour: {person.favColor}</p>

			<button on:click={() => deletePerson(person.id)}>Delete</button>
		</div>
	{:else}
		<p>There's no people to show</p>
	{/each}
</main>

<style>
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