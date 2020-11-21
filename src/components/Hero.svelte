<script>
    export let heroText;
    export let background;
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
    max-width: 650px;
    padding: 3rem 2.5rem;
    border-radius: 5px;
    text-align: center;
    color: #FEFCFB;
    font-weight: 600;
    background: rgba(3, 64, 120, 0.3) ;
}
</style>

<div style="{background}">
    <h2>{heroText}</h2>
</div>