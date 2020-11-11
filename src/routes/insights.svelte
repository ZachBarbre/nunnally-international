<script>
    import Hero from "../components/Hero.svelte";
	import Info from '../components/Info.svelte'
    import Card from "../components/Card.svelte";
    
    const heroText = 'hero text about the services we provide';
	const imgURL = 'https://picsum.photos/1900/700';

	const infoText = 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Placerat orci nulla pellentesque dignissim.'

	const firstCardContent = {
		imgUrl	: 'https://via.placeholder.com/600', 
		imgAlt: 'A discription of the image',
		text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Placerat orci nulla pellentesque dignissim.',
		header: 'Header Number One',
		background: 'background: #D6DDD9;',
		isFipped: true	
	}
	const secondCardContent = {
		imgUrl	: 'https://via.placeholder.com/600', 
		imgAlt: 'A discription of the image',
		text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Placerat orci nulla pellentesque dignissim.',
		header: 'Header Number Two',
		background: 'background: #D6DDD9;',
		// isFipped: true	
    }
    const thridCardContent = {
		imgUrl	: '', 
		imgAlt: '',
		text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Placerat orci nulla pellentesque dignissim.',
		header: 'Header Number Three',
		background: 'background: url(https://picsum.photos/1900/700) center center no-repeat;',
		isFipped: true	
	}
</script>

<svelte:head>
    <title>Our Services | Nunnally International</title>
</svelte:head>

<Hero heroText={heroText} imgURL={imgURL} />

<Info infoText={infoText} />

<Card content={firstCardContent} />
<Card content={secondCardContent} />
<Card content={thridCardContent} />