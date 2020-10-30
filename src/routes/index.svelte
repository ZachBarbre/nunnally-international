<script>
	import Card from '../components/Card.svelte';
	import Hero from '../components/Hero.svelte';
	import Info from '../components/Info.svelte';
	import BulletPoints from '../components/BulletPoints.svelte';

	const heroText = 'A string of words saying things about our company';
	const imgURL = 'https://picsum.photos/1900/700';
	const infoText = 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Placerat orci nulla pellentesque dignissim.';

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
		background: 'background: #FFFFFF;',
	}

	const bulletPointContent = {
		title: 'Header of the Bullet Points',
		points: [
			{
				img: 'https://via.placeholder.com/60',
				imgAlt: 'Discription of the image',
				header: 'Bullet Point One',
				text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor.'
			},
			{
				img: 'https://via.placeholder.com/60',
				imgAlt: 'Discription of the image',
				header: 'Bullet Point Two',
				text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor.'
			},
			{
				img: 'https://via.placeholder.com/60',
				imgAlt: 'Discription of the image',
				header: 'Bullet Point Three',
				text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor.'
			},
		],
		background: 'background: #D6DDD9;'
	}

</script>

<svelte:head>
	<title>Nunnally International</title>
</svelte:head>

<Hero heroText={heroText} imgURL={imgURL}/>

<Info infoText={infoText} />

<Card content={firstCardContent}/>

<Card content={secondCardContent}/>

<BulletPoints content={bulletPointContent} />