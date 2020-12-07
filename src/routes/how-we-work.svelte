<script>
	import Hero from "../components/Hero.svelte";
	import Info from '../components/Info.svelte';
	import Card from "../components/Card.svelte";

	const heroText = 'Perspective. Transparency. Perseverance.';
	const background = `background: url(/high-five.jpg) top 25% center no-repeat;`;
	const infoText = 'Nunnally International provides strategic M&A services to RIA firms that are looking to buy, sell or merge their business. We employ investor profiling expertise to help you find the best fit based on your strategic objectives, partnership criteria and firm culture.'

	const firstCardContent = {
		imgUrl	: '/pushing-puzzle.jpg', 
		imgAlt: 'Two men pushing large puzzle pieces together',
		text: 'We typically work with Sell-Side RIAs that are in the $100mm to $1bn AUM range (although not exclusively). Our expansive industry network extends across the United States and beyond without geographic constraints. We get to know you and your firm personally in order to gain a clear understanding of the factors that are key to your strategic partnership success - putting firm culture at the top of the list.',
		header: 'Sell-Side Advisory',
		background: 'background: #D6DDD9;',
		// isFipped: true	
	}

	const secondCardContent = {
		imgUrl	: '/handshake-light.jpg', 
		imgAlt: 'Men shaking hands',
		text: ``,
		header: 'Buy-Side Advisory',
		background: 'background: #FEFCFB',
		isFipped: true
	}

</script>

<style>
	div {
		font-size: large;
	}

	section {
		font-size: large;
	}
</style>

<svelte:head>
	<title>How We Work | Nunnally International</title>
</svelte:head>

<Hero {heroText} {background} />

<Info infoText={infoText} />

<Card content={firstCardContent}>
	<div slot="side">
		<p>
			There are generally two ways we work with sell-side RIAs, giving you an option to choose whichever best suits your specific goals and unique circumstances.
		</p>
	</div>
	<section slot="under">
		<h4>Referral</h4>
		<p>
			Nunnally International, Inc. can introduce your firm to prospective buyers through our existing referral partnerships. The groups we partner with include consolidators, as well as privately-owned independent RIAs. We make introductions in consultation with you and help facilitate the talks.  The matchmaking service is paid for by our partners, and so there is no cost to you. As a matter of principle, do not partner with anyone that we wouldn’t have manage our own money.
		</p>
		<h4>Engagement</h4>
		<p>
			RIA firms that want to sell or merge can retain Nunnally International, Inc. through an engagement agreement.  We lead the M&A process all the way from expression of interest to close.  We carefully vet prospective acquirers at the  introductory stage in order to increase the probability of a successful strategic partnership, and exercise prudent due diligence throughout the entirety of the M&A process to reduce the risk of running into problems later on.
		</p>
	</section>
</Card>
<Card content={secondCardContent}>
	<div slot="side">
		<h4>Referral Partnership Program</h4>
		<p>
			Nunnally International serves as a trusted deal source to Buy-Side RIAs through our Referral Partnership Program.  We approach our relationships with referral partners the same way that we do with sell-side RIAs. We get to know you and we go to great lengths to understand your organization's strategic objectives, partnership criteria and firm culture. We look for differentiation between our referral partners and spend the time necessary to fully comprehend your distinctive value proposition.
		</p>
	</div>
	<section slot="under">
		<p>
			When there is a good fit Nunnally International will introduce you to sell-side RIAs that have been pre-qualified and carefully vetted. We collaborate with each of our referral partners on a non-exclusive basis to ensure a level playing field.  In addition, our compensation and incentives are standardized to eliminate conflicts of interest. 
	
		</p>
		<p>
			In order to qualify for our Referral Partnership Program groups generally have to meet these three key criteria: 
		</p>
		<ul>
			<li>Proven track record of making acquisitions and successfully integrating acquired firms.</li>
			<li>Already have funding in place to make acquisitions.</li>
			<li>A level of AUM that justifies a proposed deal.</li>
		</ul>
		<p>These criteria reduce the risk to prospective sellers and increases the odds of a smooth transition post-sale.</p>
	</section>
</Card>

