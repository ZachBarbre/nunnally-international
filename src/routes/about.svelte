<script>
	import Hero from '../components/Hero.svelte';

	const heroText = 'Scratch at fleas, meow until belly rubs,';
	const imgURL = 'https://picsum.photos/1550/700';
	
</script>

<svelte:head>
	<title>About</title>
</svelte:head>

<Hero heroText={heroText} imgURL={imgURL}/>