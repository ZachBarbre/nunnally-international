<script>
	import Hero from '../components/Hero.svelte';
	import Card from '../components/Card.svelte';
	import Info from '../components/Info.svelte';
	import BulletPoints from '../components/BulletPoints.svelte';
	import { slide } from 'svelte/transition';

	const heroText = 'Perspective. Transparency. Perseverance.';
	const background = `background: url(/cheers.jpg) top 25% center no-repeat;`;
	const infoText = '';

	const firstCardContent = {
		imgUrl	: '/TylerNunnally.jpg', 
		imgAlt: 'Tyler Nunnally',
		text: `"I've spent years in the investment management industry in multiple capacities and understand the risks, opportunities challenges that advisors face on a daily basis".`,
		header: '',
		background: 'background: #D6DDD9;',
		// isFipped: true	
	}
	const secondCardContent = {
		imgUrl	: '/Prague.jpg', 
		imgAlt: 'Prague at sunset.',
		text: '"Firm culture defines how you and your team relate to one another. It is also defined by how you treat your clients.""',
		header: 'OUR APPROACH',
		background: 'background: #FFFFFF;',
		isFipped: true	
	}

	const bulletPointContent = {
		title: '',
		points: [
			{
				img: '/learn-more-global.svg',
				imgAlt: 'the earth over the palm of a hand',
				header: 'Perspective',
				text: ['Investment advisory is a people business. RIAs are relatively small and you have to work closely with the people around you. At the same time you have to manage the emotions of your clients; the fear and anxiety in down cycles, and irrational exuberance when times are good.  Firm culture defines how you and your team relate to one another. It is also defined by how you treat your clients.', 'Nunnally International puts a great deal of emphasis on firm culture because it is often the difference between a successful M&A partnership and one that fails. M&A is a lot like a marriage in that regard. No one goes into marriage expecting it to end in divorce. Our advice to buyers and sellers is to look to cultural fit first when choosing a strategic partner. Make sure that you share the same worldview, beliefs, investment philosophy and ethos. Also ensure that your short and long-term goals are aligned.']
			},
			{
				img: '/learn-more-shield.svg',
				imgAlt: 'a shield with a checkmark coat of arms',
				header: 'Transparency',
				text: ['The payoff for M&A deals is very rewarding and so the incentives to win are strong for M&A advisors, as well as buyers and sellers. The desire to win can often bring-out the worst in people, especially those that approach it with a "win at all cost" attitude. Broken promises, half truths and flat-out lies - whatever it takes. Subsequently, you have to choose your partners wisely. It is essential to dig beneath the surface through a careful vetting process at the  introductory stage, and to exercise prudent due diligence throughout the entire M&A process. We are firm believers in the Reagan era cold war adage: trust, but verify.', `At the same time, you need to be forthcoming  if there are skeletons in the closet.  It is best to get them out in the open from the onset of negotiations (after executing a mutual NDA) because it will come-out eventually. You do not want to raise doubts, insert suspicion or erode trust. It won't end well.`]
			},
			{
				img: '/learn-more-heart.svg',
				imgAlt: 'a heart lamp',
				header: 'Perseverance',
				text: ['When I first arrived in Prague I had to register my business with the Czech authorities. However, I was told (in broken English) that in order to register my business, I needed to have a commercial bank account. I went to multiple banks to try and obtain an account, and was informed by each that I needed to have a registered business before they were able to open an account on our behalf. The proverbial Catch-22. I was eventually able to maneuver around the requirements with the assistance of the America Consulate.  But I knew from that moment it was going to be rough sailing from then-on-out. It would take internal fortitude, a strong will to succeed and the ability to adapt.','The M&A process is a lot like that. It can be long and tedious with plenty of ups-and-downs along the way.  We advice clients to be mentally prepared from the onset and stick with the process despite the inevitable turmoil along the way.  It takes a toll emotionally, but you have to persevere in order to achieve your goal.']
			},
		],
		background: 'background: #77787B;',
		width: 'flex: 0 1 380px;'
	}
	
	let learnMore = false;
</script>

<style>
	p {
    	font-size: large;
		/* text-align: center; */
	}

	h3 {
		margin: 0 auto;
		text-align: center;
	}

	.title {
		margin: 0 0 10% 0;
		text-align: center;
	}

	button {
		cursor: pointer;
		font-size: large;
		padding: 1rem 2rem;
		background-color: #FDFDFD;
		border: #000000 solid 1px;
		color: #000000;
		text-decoration: none;
		border-radius: 5px;
	}

	button:hover {
		background-color: #2A2E45;
		color: #FFFFFF;
	}

	a {
		display: block;
		cursor: pointer;
		font-size: large;
		padding: 1rem 2rem;
		margin-top: 1.5rem;
		background-color: #FDFDFD;
		border: #000000 solid 1px;
		color: #000000;
		text-decoration: none;
		border-radius: 5px;
		max-width: 200px;
		text-align: center;
	}

	a:hover {
		background-color: #2A2E45;
		color: #FFFFFF;
	}

	.learn {
		background-color: #2A2E45;
		color: #FFFFFF;
	}

	.learn:hover {
		background-color: #FDFDFD;
		color: #000000;
	}

	.additional {
		margin: 0 auto;
		padding: 2% 0 0;
		width: 85%;
		min-width: 300px;
		max-width: 1350px;
	}

	.additional p {
    	font-size: 18px;
    	text-align: left;
	}

	.learn-more {
		margin: 0 auto 4rem;
		padding: 0;
		width: 68%;
		min-width: 300px;
		max-width: 1350px;
	}

	.learn-more p {
    	font-size: 18px;
    	text-align: left;
	}

	@media (max-width: 1024px) {
		.additional {
			width: 65%;
			max-width: 500px;
		}
	}

	@media (max-width: 430px) {
		.additional {
			width: 90%;
			min-width: 272px;
		}

		a {
			margin-left: auto;
			margin-right: auto;
		}
	}
</style>

<svelte:head>
	<title>About | Nunnally International</title>
</svelte:head>

<Hero heroText={heroText} background={background}/>
<Info infoText={infoText} />s

<Card content={firstCardContent}>
	<div slot="side">
		<h3>Tyler Nunnally</h3>
		<p class="title">Founder & CEO</p>
		<p>
			Tyler founded Nunnally International, Inc. to focus exclusively on the RIA market after serving as the Head of FinTech at M&A advisory EGL Holdings. Founded in 1988 as a merchant banking firm, EGL Holdings has over 200 mergers, acquisitions and global capital raise transactions to its credit.
		</p>
		<p>
			Prior entering M&A, Tyler served as a strategist to leading advisor technology companies – including investor risk profiling provider FinaMetrica, which was acquired by Morningstar.  He began his career in the wealth management industry as an executive at Oxford University spin-off consultancy, Oxford Risk.
		</p>
		<p>
			Tyler has consulted hundreds of RIAs on matters of risk as a frequent speaker at industry conferences, host of countless webinars and key relationship manager to strategic partners at SEI Investments, TD Ameritrade, LPL, Fidelity, Schwab, Redtail, Orion Advisor Services, MoneyGuidePro and Fi360.

		</p>
	</div>
	<article slot="under" class='additional'>
		
		<p>
			As an industry thought-leader, he has been published widely and interviewed extensively by The Wall Street Journal, Bloomberg, CNBC, Smart Money, Kiplinger and InvestmentNews. In addition to his work in M&A, Tyler serves as an expert witness in FINRA arbitration disputes and has consulted in multibillion-dollar class action lawsuits, including the BP oil spill in the Gulf of Mexico. 
		</p>
		<p>
			Tyler began his career as a budding entrepreneur in Eastern Europe following the collapse of communism. He has lived in the Czech Republic, Scotland, England and Spain. He currently resides in his hometown Atlanta with his wife Eva and their two teenage sons.  Max is a promising high school athlete and Dylan is a Biochemistry major at University College Dublin in Ireland.
		</p>
		<p>
			Tyler holds a B.A. from the University of Georgia and a Master’s in International Business with Distinction from the University of St Andrews in Scotland.
		</p>
		<a href="/Tyler D. Nunnally Professional Biography.pdf" target="_blank" >Professional Biography</a>
	</article>
</Card>
<Card content={secondCardContent}>
	<div slot="side">
		<p>My career path took some interesting twists and turns before I joined the wealth management industry in 2006 and eventually moved into M&A. The experiences taught me 3 important lessons that explain Nunnally International's approach to M&A and the emphasis we put on strategic objectives, partnership criteria and firm culture to help you find the best fit. It also provides a good indication of what you can expect from us.</p>
		<button class="learn" on:click={() => learnMore = !learnMore}>LEARN MORE</button>
	</div>
</Card>
{#if learnMore}
	<article class='learn-more' transition:slide>
		<p>
			I did not start-out as an analyst at an investment bank or work for a  Wall Street firm. I began my career as  a 24-year old entrepreneur in Prague, Czech Republic following the collapse of communism in Eastern Europe. I worked in the country throughout the transition from communism to capitalism, and witnessed first-hand how money can bring-out the best and worst in people. 
		</p>
		<p>
			During those days the Czech Republic was a highly unregulated market with few protections against trickery, fraud and deceit. It was truly a Kafkaesque reality where things often were not as they seemed.  To survive and thrive in that environment you had to navigate risks that went beyond the numbers. You had to understand the motivations and incentives that strike at the core human nature
		</p>
		<p>
			I sold the business after a successful ten-year run and later joined Oxford University spin-off consultancy, Oxford Risk. I was responsible commercializing the company's investor risk profiling research and worked alongside a team of prominent Oxford academics to bring the product to market.  It proved to be an excellent training ground for an education in behavioral finance which is very beneficial in M&A where biases like endowment effect, confirmation bias and time discounting routinely surface during negotiations.  
		</p>
	</article>
{/if}
<BulletPoints content={bulletPointContent} />
