<script lang="ts">
	import Nested from './Nested.svelte';
	import Auth from './Auth.svelte';
	import Arithmetic from './Arithmetic.svelte';
	import Cats from './Cats.svelte';
	import Things from './Things.svelte';
	import RandomNumber from './RandomNumber.svelte';

	export let name: string;
</script>

<main>
	<h1>Hello {name}!</h1>
	<p>Visit the <a href="https://svelte.dev/tutorial">Svelte tutorial</a> to learn how to build Svelte apps.</p>
	<Nested answer={42.34567}/>
	<Auth/>
	<Arithmetic x={189}/>
	<Cats/>
	<Things/>
	<RandomNumber/>
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
