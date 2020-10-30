<script>
	import Hero from "../components/Hero.svelte";
	import Card from "../components/Card.svelte";

	const heroText = 'The hero text discribing our advantage';
	const imgURL = 'https://picsum.photos/1900/700';

	const firstCardContent = {
		imgUrl	: '', 
		imgAlt: '',
		text: 'This will be a contact form if you would like. They normally come to you as emails. I do not find them useful but it is up to you. Typical fields are Name, email, subject, and message',
		header: 'Contact Form',
		background: 'background: url("https://picsum.photos/1900/700") center center no-repeat;',
		isFipped: true	
	}
</script>

<style>
	section {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }

    h2 {
        margin: 5rem 0 2rem 0;
        text-align: center;
    }
    .point-container {
        width: 70%;
        display: flex;
        justify-content: space-evenly;
        align-items: center;
        flex-flow: row wrap;
    }
    .point {
        
        display: flex;
        flex-direction: column;
        align-items: center;
        background: #FFF;
        padding: 4% 2%;
        margin: 5% 0;
    }

    h4 {
		font-weight: 600;
        padding: 1.5rem 0 1rem 0;
        font-size: 1.4rem;
		margin: 0;
    }

	address {
		font-style: normal;
		font-size: 1rem;
		text-align: center;
	}

	a {
		font-weight: 600;
		text-decoration: none;
	}
</style>

<svelte:head>
	<title>Contact | Nunnally International</title>
</svelte:head>

<Hero heroText={heroText} imgURL={imgURL}/>

<section>
    <h2>Contact Information</h2>
    <div class="point-container">
		<div class="point">
			<h4>Location</h4>
			<address>Your address if you would like it</address>
		</div>
		<div class="point">
			<h4><a href="mailto:tyler.nunnally@gmail.com">tyler.nunnally@gmail.com</a></h4>
			<address>555-555-5555</address>
		</div>
    </div>
</section>

<Card content={firstCardContent} />


