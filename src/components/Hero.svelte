<script>
    export let heroText;
    export let background;
</script>

<style>
div { 
    margin: 0 auto;
    background-size: cover;
    width: 100%;
    height: 55vh;
    display: flex;
    justify-content: center;
    align-items: center;
    max-width: 1920px;
}

h2 {
    width: 70%;
    max-width: 650px;
    font-size: 24px;
    padding: 1.5rem 1.25rem;
    border-radius: 5px;
    text-align: center;
    color: #FEFCFB;
    background: rgba(3, 64, 120, 0.3);
}
</style>

<div style="{background}">
    <h2>{heroText}</h2>
</div>