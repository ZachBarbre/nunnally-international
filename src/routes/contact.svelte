<script>
    import Hero from '../components/Hero.svelte';
    import { faPhone, faEnvelopeOpen, faMapMarkerAlt } from '@fortawesome/free-solid-svg-icons';
    import { faTwitterSquare, faLinkedin } from '@fortawesome/free-brands-svg-icons';
    import Icon from 'fa-svelte';

	const heroText = 'Perspective. Transparency. Perseverance.';
	const background = `background: url(/Atlanta.jpg) top center no-repeat;`;
	
</script>

<style>
	section {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }

    .img-wrapper {
        display: flex;
        margin: 2% auto;
    }

    img {
        height: auto;
        width: 100%;
    }

    h2 {
        margin: 2rem 0;
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
        align-items: flex-start;
        background: #FFF;
        padding: 4% 2%;
        margin: 5% 0;
    }

    .contact-item {
        display: flex;
        justify-content: start;
        align-items: center;
        padding: 0.5rem 0;
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
        padding: 0 0 0 1rem;
	}

	a {
        font-size: 1.5rem;
		text-decoration: none;
        padding: 0 0 0 1rem;
	}

    .socal-icon {
        font-size: 2rem;
        padding-top: 3px;
    }

    @media (max-width: 360px) {
        a {
            font-size: 1.2rem;
        }
    }
</style>

<svelte:head>
	<title>Contact | Nunnally International</title>
</svelte:head>

<Hero {heroText} {background}/>

<section>
    <div class="img-wrapper">
        <img src="/logo-large.png" alt="Nunnally International Logo">
    </div>
    <h2>Contact Us</h2>
    <div class="point-container">
		<div class="point">
            <div class="contact-item">
                <Icon icon={faPhone}></Icon>
                <address>+1 404 492 2152</address>
            </div>
            <div class="contact-item">
                <Icon icon={faEnvelopeOpen}></Icon>
                <a href="mailto:info@nunnallyinternational.com">info@nunnallyinternational.com</a>
            </div>
            <div class="contact-item">
                <Icon icon={faMapMarkerAlt}></Icon>
                <address>Atlanta, Georgia, USA</address>
            </div>
		</div>
		<div class="point">
			<h4>Connect with Us on Social Media</h4>
			<!-- <div class="contact-social">
                <a class="social" href="https://twitter.com/tylerdnunnally/">
                    <Icon icon={faTwitterSquare}></Icon>
                </a>
                <a class="social" href="https://www.linkedin.com/in/tylernunnally/">
                    <Icon icon={faLinkedin}></Icon>
                </a>
            </div> -->
            <div class="contact-item">
                <a href="https://twitter.com/tylerdnunnally/" class="socal-icon">
                    <Icon icon={faTwitterSquare}></Icon>
                </a>
                <a href="https://twitter.com/tylerdnunnally/">Twitter</a>
            </div>
            <div class="contact-item">
                <a href="https://www.linkedin.com/in/tylernunnally/" class="socal-icon">
                    <Icon icon={faLinkedin}></Icon>
                </a>
                <a href="https://www.linkedin.com/in/tylernunnally/">Linkedin</a>
            </div>
		</div>
    </div>
</section>


