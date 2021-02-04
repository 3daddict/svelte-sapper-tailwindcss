<script>
	import Nav from '../components/Nav.svelte';

	export let segment;
</script>

<style global lang="postcss">
	@tailwind base;
	@tailwind components;
	@tailwind utilities;
	
	/* Add Global Styles Below */
</style>

<Nav {segment}/>

<main>
	<slot></slot>
</main>