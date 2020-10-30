<script>
	import Hero from '../components/Hero.svelte';
	import Card from '../components/Card.svelte';
	import Info from '../components/Info.svelte';

	const heroText = 'A Header describing  our company';
	const imgURL = 'https://picsum.photos/1550/700';
	const infoText = 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Risus viverra adipiscing at in tellus. Vel pharetra vel turpis nunc eget lorem dolor sed viverra. Pharetra convallis posuere morbi leo urna molestie at elementum eu. Bibendum est ultricies integer quis auctor elit sed vulputate mi. Nec nam aliquam sem et tortor consequat id porta nibh. Quis auctor elit sed vulputate mi sit amet mauris. Mattis vulputate enim nulla aliquet porttitor. Suspendisse sed nisi lacus sed viverra tellus in hac. Proin sed libero enim sed. Id faucibus nisl tincidunt eget nullam non nisi. Lectus magna fringilla urna porttitor rhoncus dolor purus non enim.';

	const firstCardContent = {
		imgUrl	: 'https://via.placeholder.com/600', 
		imgAlt: 'A discription of the image',
		text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Placerat orci nulla pellentesque dignissim.',
		header: 'Header Number One',
		background: 'background: #D6DDD9;',
		// isFipped: true	
	}
</script>

<style>
	p {
    	font-size: 1.2rem;
	}

	a {
		font-size: larger;
		padding: 1rem 2rem;
		background-color: #FDFDFD;
		border: #000000 solid 1px;
		color: #000000;
		text-decoration: none;
		border-radius: 5px;
	}

	a:hover {
		background-color: #2A2E45;
		color: #FFFFFF;
	}
</style>

<svelte:head>
	<title>About | Nunnally International</title>
</svelte:head>

<Hero heroText={heroText} imgURL={imgURL}/>
<Info infoText={infoText}>
	<p>
		Tellus in metus vulputate eu scelerisque felis imperdiet proin fermentum. Suspendisse potenti nullam ac tortor vitae purus faucibus ornare. Eget est lorem ipsum dolor sit amet consectetur adipiscing. Quis imperdiet massa tincidunt nunc pulvinar sapien et. Ipsum dolor sit amet consectetur adipiscing elit. Donec pretium vulputate sapien nec. Facilisi morbi tempus iaculis urna id volutpat lacus laoreet. A diam maecenas sed enim ut sem viverra. Enim nulla aliquet porttitor lacus luctus accumsan tortor posuere. Magna sit amet purus gravida. Facilisis sed odio morbi quis commodo odio aenean. Nunc vel risus commodo viverra maecenas accumsan lacus vel. Vulputate sapien nec sagittis aliquam malesuada bibendum arcu vitae elementum. Proin sagittis nisl rhoncus mattis rhoncus. A condimentum vitae sapien pellentesque habitant.
	</p>
</Info>

<Card content={firstCardContent}>
	<a href="contact">Contact Us</a>
</Card>
