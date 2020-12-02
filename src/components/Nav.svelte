<script>
	import Icon from 'fa-svelte';
	import { faBars, faTimes } from '@fortawesome/free-solid-svg-icons';
	import { slide } from 'svelte/transition';
	export let segment;

	let menuBars = faBars;

	let isMobileMenuOpen = false;

	const handleMenu = () => {
		menuBars = menuBars === faBars ? faTimes : faBars;
		isMobileMenuOpen = !isMobileMenuOpen;
	}

</script>

<style>
	nav {
		display: flex;
		justify-content: space-around;
		align-items: center;
		border-bottom: 1px solid rgba(255,62,0,0.1);
		font-weight: 300;
		padding: 0 1em;
		width: 80%;
	}

	.nav-menu {
		margin: 0;
		padding: 0;
		display: flex;
		justify-content: space-around;
		min-width: 550px;
	}

	/* clearfix */
	.nav-menu::after {
		content: '';
		display: block;
		clear: both;
	}

	.logo-nav {
		padding: .5rem 1rem 0 0;
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
		background-color: #00A9E1;
		display: block;
		bottom: -1px;
	}

	a {
		text-decoration: none;
		padding: 0.5em 0.5em;
		display: block;
		font-size: larger;
	}


	#mobile-menu-button {
		display: none;
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

		.nav-menu-mobile {
			display: flex;
			flex-direction: column;
			align-items: flex-end;
			position: absolute;
			top: 85px;
			right: 5%;
			z-index: 99;
			background-color:#FFF;
			border: lightgray 1px solid;
			padding: 1px 0 5px 0; 
			width: 30%;
			min-width: 160px;
		}

		#mobile-menu-button {
		display: block;
		}

		div :global(.size-3x) {
   			font-size: 25px;
  		}
	}
</style>

<nav>
	<div class="logo-nav">
		<img 
			srcset="/logo.png 150w, /logo-medium.png 225w"
			sizes="(max-width: 420px) 150px, 225px"
			src="/logo.png" 
			alt="Nunnally International">
	</div>
	<ul class="nav-menu">
		<li><a aria-current="{segment === undefined ? 'page' : undefined}" href=".">Home</a></li>
		<li><a aria-current="{segment === 'how-we-work' ? 'page' : undefined}" href="how-we-work">How We Work</a></li>
		<li><a aria-current="{segment === 'about' ? 'page' : undefined}" href="about">About Us</a></li>
		<li><a aria-current="{segment === 'insights' ? 'page' : undefined}" href="insights">News & Insights</a></li>
		<li><a aria-current="{segment === 'contact' ? 'page' : undefined}" href="contact"> Contact</a></li>
	</ul>
	{#if isMobileMenuOpen}
		<ul class="nav-menu-mobile" on:click="{handleMenu}" transition:slide>
			<li><a aria-current="{segment === undefined ? 'page' : undefined}" href=".">Home</a></li>
			<li><a aria-current="{segment === 'how-we-work' ? 'page' : undefined}" href="how-we-work">How We Work</a></li>
			<li><a aria-current="{segment === 'about' ? 'page' : undefined}" href="about">About Us</a></li>
			<li><a aria-current="{segment === 'insights' ? 'page' : undefined}" href="insights">Insights</a></li>
			<li><a aria-current="{segment === 'contact' ? 'page' : undefined}" href="contact"> Contact</a></li>
		</ul>
	{/if}
	<div id="mobile-menu-button" on:click={handleMenu}>
		<Icon icon={menuBars} class="size-3x"></Icon>
	</div>
</nav>
