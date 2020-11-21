<script>
    import Hero from "../components/Hero.svelte";
	import Info from '../components/Info.svelte';
	import Reports from "../components/Reports.svelte";
    
	const heroText = 'Perspective. Transparency. Perseverance.';
	const background = `background: url(/high-five.jpg) top 25% center no-repeat;`;

	const reportsInfoText = 'Market Intelligence: Access our latest market analysis and research on the RIA M&A market';

	const reports = {reports: [
		{
			title: 'How Much is My RIA Worth?',
			description: 'Evaluation of the impact of Covid-19 and subsequent market volatility on valuations.',
			downloadURI: '/RIA M&A Market Report - How Much is My RIA Worth.pdf'
		},
		{
			title: 'Is It the Right Time to Sell?',
			description: 'Analysis of the 3 primary factors that are driving RIA M&A deals to record highs.',
			downloadURI: '/RIA M&A MARKET REPORT - Is it the Right Time to Sell.pdf'
		},
	]};

	const dealsInfoText = 'M&A Deals: Our most recently completed transactions';
</script>

<svelte:head>
    <title>Our Services | Nunnally International</title>
</svelte:head>

<Hero {heroText} {background} />

<Info infoText={reportsInfoText} />

<Reports {reports} />

<Info infoText={dealsInfoText} />

