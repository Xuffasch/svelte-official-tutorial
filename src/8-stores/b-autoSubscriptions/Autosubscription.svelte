<script>
	import { count } from './stores.js';
	import Incrementer from './Incrementer.svelte';
	import Decrementer from './Decrementer.svelte';
	import Resetter from './Resetter.svelte';
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
  }
</style>

<div class='chapter-display'>
  <h1 class="chapter">b - Auto-subscriptions</h1>
  <h1>The count is {$count}</h1>

  <span>
    <Incrementer/>
    <Decrementer/>
    <Resetter/>
  </span>

</div>
