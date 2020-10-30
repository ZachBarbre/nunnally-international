<script>
    export let segment;
    import Icon from 'fa-svelte';
    import { faFacebookSquare, faLinkedin } from '@fortawesome/free-brands-svg-icons';
</script>

<style>
    footer {
        margin: 5% 0;
        display: flex;
        flex-direction: column;
        align-items: center;
    }

    h2 {
        text-align: center;
    }

    ul {
        padding: 2% 5% 1% 5%;
        /* margin: 2% auto; */
        display: flex;
        flex-flow: row wrap;
        justify-content: space-evenly;
        
    }

    li {
        list-style: none;
        margin: 1% 0;
        padding: 0 0.5rem;
        font-size: 18px;
    }

    li a {
        text-decoration: none;
    }

    .selected {
        color: #6fafd7;
    }

    .social {
        font-size: 30px;
        color: lightgray;
        padding: 0 5px;
    }
    
</style>

<footer>
    <h2>Nunnally International, Inc</h2>
    
    <ul>
        <li><a class:selected="{segment === undefined}" href=".">Home</a></li>
        <li><a class:selected="{segment === 'advantage'}" href="advantage">Our Advantage</a></li>
        <li><a class:selected="{segment === 'services'}" href="services">Our Services</a></li>
        <li><a class:selected="{segment === 'about'}" href="about">About Us</a></li>
        <li><a class:selected="{segment === 'contact'}" href="contact">Contact</a></li>
    </ul>
    
    <div>
        <a class="social" href="#"><Icon icon={faFacebookSquare} class="social"></Icon></a>
        <a class="social" href="#"><Icon icon={faLinkedin} class="social"></Icon></a>
    </div>
    <p>5555 Vistmont Drive, Decatur GA 300033, United States</p>
    <p><strong><a href="mailto:tyler.nunnally@gmail.com>">tyler.nunnally@gmail.com</a> | 555-555-5555</strong></p>
</footer>