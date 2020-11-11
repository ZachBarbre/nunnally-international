<script>
	import Hero from "../components/Hero.svelte";

	const heroText = 'Perspective. Transparency. Perseverance.';
	const imgURL = 'https://picsum.photos/1900/700';

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
		font-size: 1.5rem;
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
			<h4>Tyler Nunnally</h4>
		</div>
		<div class="point">
			<h4><a href="mailto:info@NunnallyInternational.com">info@NunnallyInternational.com</a></h4>
			<address>404 492 2152</address>
		</div>
    </div>
</section>


