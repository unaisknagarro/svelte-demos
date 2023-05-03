<script>
	import { count } from './stores.js';
	import {onDestroy} from 'svelte';
	import Incrementer from './Incrementer.svelte';
	import Decrementer from './Decrementer.svelte';
	import Resetter from './Resetter.svelte';

	let countValue;

	let subscription = count.subscribe(value => {
		countValue = value;
	});

	onDestroy(subscription);
</script>

<h1>The count is {countValue}</h1>

<Incrementer/>
<Decrementer/>
<Resetter/>
