<script>
    export let heroText;
    export let imgURL;
    const background = `background: url(${imgURL}) center center no-repeat fixed;`;
</script>

<style>
div { 
    background-size: cover;
    width: 100%;
    height: 70vh;
    display: flex;
    justify-content: center;
    align-items: center;
}

h2 {
    width: 70%;
    text-align: center;
    color: white;
    text-shadow: 0px 14px 70px rgba(0, 0, 0, 0.7);
    font-weight: 500;
}
</style>

<div style="{background}">
    <h2>{heroText}</h2>
</div>