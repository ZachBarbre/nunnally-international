<script>
	import Hero from '../components/Hero.svelte';
	import Card from '../components/Card.svelte';

	const heroText = 'A Header describing  our company';
	const imgURL = 'https://picsum.photos/1550/700';
	
</script>

<svelte:head>
	<title>About</title>
</svelte:head>

<Hero heroText={heroText} imgURL={imgURL}/>

