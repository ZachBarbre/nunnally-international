<script>
	import Icon from 'fa-svelte';
	import { faBars, faTimes } from '@fortawesome/free-solid-svg-icons';
	export let segment;

	let menuBars = faBars;

	const handleMenu = () => {
		menuBars = menuBars === faBars ? faTimes : faBars;
	}

</script>

<style>
	nav {
		display: flex;
		/* justify-content: space-between; */
		border-bottom: 1px solid rgba(255,62,0,0.1);
		font-weight: 300;
		padding: 0 1em;
		width: 80%;
	}

	.nav-menu {
		margin: 0;
		padding: 0;
		display: flex;
		justify-content: space-evenly;
		min-width: 550px;
	}

	/* clearfix */
	.nav-menu::after {
		content: '';
		display: block;
		clear: both;
	}

	.logo-nav {
		padding: 0 1rem;
	}

	li {
		display: block;
		float: left;
	}

	[aria-current] {
		position: relative;
		display: inline-block;
	}

	[aria-current]::after {
		position: absolute;
		content: '';
		width: calc(100% - 1em);
		height: 2px;
		background-color: #6fafd7;
		display: block;
		bottom: -1px;
	}

	a {
		text-decoration: none;
		padding: 0.5em 0.5em;
		display: block;
		font-size: larger;
	}

	@media (max-width: 1000px) {
		nav {
			justify-content: space-between;
			align-items: center;
			padding: 0 0;
			margin: 1em auto;
			width: 90%;
		}
		.nav-menu {
			display: none;
		}

		div :global(.size-4x) {
   			font-size: 40px;
  		}
	}
</style>

<nav>
	<div class="logo-nav">
		<img src="http://via.placeholder.com/150X60" alt="Logo for the Company">
	</div>
	<ul class='nav-menu'>
		<li><a aria-current="{segment === undefined ? 'page' : undefined}" href=".">Home</a></li>
		<li><a aria-current="{segment === 'advantage' ? 'page' : undefined}" href="advantage">Our Advantage</a></li>
		<li><a aria-current="{segment === 'services' ? 'page' : undefined}" href="services">Our Services</a></li>
		<li><a aria-current="{segment === 'about' ? 'page' : undefined}" href="about">About Us</a></li>
		<li><a aria-current="{segment === 'contact' ? 'page' : undefined}" href="contact"> Contact</a></li>
	</ul>
	<div on:click={handleMenu}>
		<Icon icon={menuBars} class="size-4x"></Icon>
	</div>
</nav>
