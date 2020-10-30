<script>
	import Hero from "../components/Hero.svelte";
	import Info from '../components/Info.svelte'
	import Card from "../components/Card.svelte";
import BulletPoints from "../components/BulletPoints.svelte";


	const heroText = 'The hero text discribing our advantage';
	const imgURL = 'https://picsum.photos/1900/700';

	const infoText = 'A sentence about the advatage we provide to our clients. Lorem ipsum dolor sit amet, consectetur adipiscing elit.'

	const firstCardContent = {
		imgUrl	: 'https://via.placeholder.com/600', 
		imgAlt: 'A discription of the image',
		text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Placerat orci nulla pellentesque dignissim.',
		header: 'Header Number One',
		background: 'background: #D6DDD9;',
		// isFipped: true	
	}

	const secondCardContent = {
		imgUrl	: '', 
		imgAlt: 'A discription of the image',
		text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Placerat orci nulla pellentesque dignissim.',
		header: 'Header Number Two',
		background: 'background: url("https://picsum.photos/1900/700") center center no-repeat;',
		// isFipped: true	
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
		],
		background: 'background: #FFFFFF;'
	}

</script>

<style>
	a {
		font-size: larger;
		padding: 1rem 2rem;
		background-color: #2A2E45;
		border: #000000 solid 1px;
		color: #FFFFFF;
		text-decoration: none;
		border-radius: 5px;
	}

	a:hover {
		background-color: #FDFDFD;
		color: #000000;
	}
</style>

<svelte:head>
	<title>Our Advantage | Nunnally International</title>
</svelte:head>

<Hero heroText={heroText} imgURL={imgURL} />

<Info infoText={infoText} />

<Card content={firstCardContent} />

<Card content={secondCardContent}>
	<a href="contact">Contact Us</a>
</Card>

<BulletPoints content={bulletPointContent}/>
