<script>
	import Writable from './8-stores/a-writable/Writable.svelte'
	import AutoSubscriptions from './8-stores/b-autoSubscriptions/Autosubscription.svelte'
	export let name;
</script>

<main>
	<h1>Hello {name}!</h1>
	<p>Visit the <a href="https://svelte.dev/tutorial">Svelte tutorial</a> to learn how to build Svelte apps.</p>
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

	.chapter-title {
		font-size: x-large;
		color: red;
	}

	section {
		max-width: 240px;
		display: flex;
		flex-direction: column;
		margin: 0 auto;
	}
</style>

<section>
	<h1 class='chapter-title'> 8 - Stores </h1>
	<Writable />
	<AutoSubscriptions />
</section>

