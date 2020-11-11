<script>
	import Card from '../components/Card.svelte';
	import Hero from '../components/Hero.svelte';
	import Info from '../components/Info.svelte';
	import BulletPoints from '../components/BulletPoints.svelte';

	const heroText = 'Perspective. Transparency. Perseverance.';
	const imgURL = 'https://picsum.photos/1900/700';
	const infoText = 'Nunnally International provides strategic M&A services to RIA firms that are looking to buy, sell or merge their business.';

	const firstCardContent = {
		imgUrl	: '/financial-advice.jpg', 
		imgAlt: 'A older couple receiving financial advice.',
		text: "We've spent years in the investment management industry in multiple capacities and understand the risks, opportunities and challenges that advisors face on a daily basis. We understand that every RIA is uniquely different and we tailor our  M&A guidance to your specific goals and circumstances.",
		background: 'background: #D6DDD9;',
		header: 'MARKET KNOWLEDGE',
	}

	const secondCardContent = {
		imgUrl	: '/buisness-handshake.jpg', 
		imgAlt: 'Two men shaking hands with a third standing behind.',
		text: "We act in your best interest by adhering to the same fiduciary principles and standard of care that you do. Our incentives are always aligned with yours and we're only compensated if your M&A deal successfully closes.",
		header: 'UNCONFLICTED ADVICE', 
		background: 'background: #fefcfb;',
		isFipped: true	
	}

	const bulletPointContent = {
		title: "How We're Different",
		points: [
			{
				img: '/bullet-1-target.svg',
				imgAlt: 'An arrow hitting a bullseye',
				header: 'Strategic Objectives',
				text: 'What are your goals and how can M&A help you achieve them? Is your intent to grow, diversify, adapt or create a succession plan?'
			},
			{
				img: '/bullet-2-handshake.svg',
				imgAlt: 'Handshake',
				header: 'Partnership Criteria',
				text: "Who can help you achieve your objectives? What characteristics define an ideal strategic partner? What's that's profile look like?"
			},
			{
				img: '/bullet-3-puzzle.svg',
				imgAlt: 'Interlocking puzzle pieces',
				header: 'Firm Culture',
				text: 'Do you share the same worldview, investment philosophy and ambitions? What synergies exists professionally and personally between firm principles?'
			},
		],
		background: 'background: #D6DDD9;'
	}

</script>

<style>
	p {
		width: 75%;
		text-align: center;
		font-size: 1.2rem;
		max-width: 1200px;
	}
</style>

<svelte:head>
	<title>Nunnally International</title>
</svelte:head>

<Hero heroText={heroText} imgURL={imgURL}/>

<Info infoText={infoText} />

<Card content={firstCardContent} />

<Card content={secondCardContent}/>

<BulletPoints content={bulletPointContent}>
	<p>Nunnally International employs investor profiling expertise to help you find the best fit.  We get to know you and your firm personally in order to gain a clear understanding of the factors that are key to your strategic partnership success. </p>
</BulletPoints>