<script>
	import { count } from './stores.js';
	import Incrementer from './Incrementer.svelte';
	import Decrementer from './Decrementer.svelte';
	import Resetter from './Resetter.svelte';

	let count_value;

  // unsubscribe fonction to run on destroy of the component to avoid memory leak
  import { onDestroy } from 'svelte' 
	const unsubscribe = count.subscribe(value => {
		count_value = value;
	});

  onDestroy(unsubscribe)

</script>

<style>
  .chapter-display {
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
    text-align: center;
  }

  .chapter {
    font-size: large;
    font-weight: 400;
  }
</style>

<h1 class='chapter'>a - Writeable stores</h1>
<div class='chapter-display'>
  <h1>The count is {count_value}</h1>
  <span>
    <Incrementer/>
    <Decrementer/>
    <Resetter/>
  </span>
</div>
