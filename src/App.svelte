<script>
	import About from "./components/About.svelte"
	import Text from "./components/Text.svelte";
	import Person from "./components/Person.svelte"
	export let name;
	export let lastName;
	let svelteLogo= 'https://arepa.s3.amazonaws.com/svelte-logo.png'
	const data ={
		name: 'Jorge',
		lastName: 'Mejia',
		age:33,
	}
</script>

<main>
	<h1>Hello {name} {lastName}!</h1>
	<About />
	<Text anotherText="hola"/>
	<Text />
	<Person {...data}/>
	<img src={svelteLogo} alt="Svelte"/>
</main>

<style>

	:global(body) {
		background-color: #f2eee2;
		color: #0084f6
	}

	:global(:root) {
		--theme-color: purple;
	}
	main img {
		width: 30%;
	}
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