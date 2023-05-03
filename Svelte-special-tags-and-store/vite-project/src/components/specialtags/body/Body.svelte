<script>
	let inside = false;

	const handleMouseenter = () => inside = true;
	const handleMouseleave = () => inside = false;

    $: console.log('inside',inside)
</script>

{inside}
<svelte:body
	on:mouseenter={handleMouseenter}
	on:mouseleave={handleMouseleave}
/>


<style>

</style>
