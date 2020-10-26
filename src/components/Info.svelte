<script>
    export let infoText;
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
</style>

<div>
    <p>{infoText}</p>
    <slot></slot>
</div>