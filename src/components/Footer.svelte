<script>
    export let segment;
    import Icon from 'fa-svelte';
    import { faTwitterSquare, faLinkedin } from '@fortawesome/free-brands-svg-icons';
</script>

<style>
    footer {
        margin: 5% 0;
        display: flex;
        flex-direction: column;
        align-items: center;
    }

    a {
        text-decoration: none;
    }

    li {
        list-style: none;
    }

    ul.nav {
        padding: 2% 5% 1% 5%;
        /* margin: 2% auto; */
        display: flex;
        flex-flow: row wrap;
        justify-content: space-evenly;
        
    }

    ul.nav > li {
        margin: 1% 0;
        padding: 0 1.4rem;
        font-size: 18px;
    }

    .selected {
        color: #00A7E2;
    }

    .social {
        font-size: 30px;
        color: lightgray;
        padding: 0 5px;
    }

    .social:hover {
        color: #034078;
    }

    .copyright {
        font-size: small;
        margin-top: 2%;
    }
    
    ul.contact {
        padding-inline-start: 0;
        width: 90%;
        margin: 0 auto;
        display: flex;
        justify-content: center;
        flex-wrap: wrap;
    }
    
    ul.contact > li {
        padding: 1% 1%;
    }
</style>

<footer>   
    <ul class="nav">
        <li><a class:selected="{segment === undefined}" href=".">Home</a></li>
        <li><a class:selected="{segment === 'how-we-work'}" href="how-we-work">How We Work</a></li>
        <li><a class:selected="{segment === 'about'}" href="about">About Us</a></li>
        <li><a class:selected="{segment === 'insights'}" href="insights">News & Insights</a></li>
        <li><a class:selected="{segment === 'contact'}" href="contact"> Contact</a></li>
    </ul>
    
    <div>
        <a class="social" href="https://www.linkedin.com/company/nunnally-international-inc" aria-label="Nunnaly International Linkedin">
            <Icon icon={faLinkedin} class="social"></Icon>
        </a>
        <a class="social" href="https://twitter.com/tylerdnunnally/" aria-label="Nunnally International Twitter">
            <Icon icon={faTwitterSquare} class="social"></Icon>
        </a>
    </div>
    <ul class="contact">
        <li>Nunnally International, Inc.</li>
        <li>|</li>
        <li>Atlanta Georgia, USA</li>
        <li>|</li>
        <li><strong><a href="mailto:info@NunnallyInternational.com">info@NunnallyInternational.com</a></strong></li>
        <li>|</li>
        <li>+1 404 492 2152</li>
    </ul>
    <p class='copyright'>©2020 Nunnally International, Inc. ALL RIGHTS RESERVED.</p>
</footer>