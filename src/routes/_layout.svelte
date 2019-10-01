<script>
	import Nav from '../components/Nav.svelte';

	export let segment;
</script>

<style>
	main {
		position: relative;
		/* max-width: 56em; */
		max-width: 1200px;
		/* background-color: white; */
		padding: 2em;
		margin: 0 auto;
		/* margin: 80px auto 0; */
		box-sizing: border-box;  
	}
</style>

<Nav {segment}/>

<main>
	<slot></slot>
</main>