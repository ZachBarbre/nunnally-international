<script>
    export let infoText;
    export let location;
</script>

<style>
div {
    margin: 0 auto;
    padding: 50px 0;
    width: 80%;
    text-align: center;
}

p {
    font-size: 1.2rem;
}

.italic {
    font-style: italic;
}
</style>

<div>
    <p class:italic="{location === 'about'}">{infoText}</p>
    <slot></slot>
</div>