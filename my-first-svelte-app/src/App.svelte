<script lang="ts">
  import Name from './Name.svelte';
  export let name = 'Unais';
  export let details ={
    name: 'Unais',
    lastname: 'Kamle',
    organization: 'Nagarro',
    age: 30
  };

  let cats = [
		{ id: 'J---aiyznGQ', name: 'Keyboard Cat' },
		{ id: 'z_AbfPXTKms', name: 'Maru' },
		{ id: 'OUtn3pvWmpg', name: 'Henri The Existential Cat' }
	];

  let x=5;
</script>

{#if x>10}
<p>
  X is greater than 10
</p>
{:else if x == 5}
<p>
  X is equal to 5
</p>
{:else}
<p>
  X is less than 10
</p>
{/if}

{#each cats as { id, name }, i}
		<li><a target="_blank" href="https://www.youtube.com/watch?v={id}" rel="noreferrer">
			{i + 1}: {name}
		</a></li>
	{/each}

