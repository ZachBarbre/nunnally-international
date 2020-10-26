<script>
    export let content;
    const { imgUrl, imgAlt, text, header, background } = content;
</script>

<style>
.card {
    display: flex;
    flex-flow: row wrap;
    justify-content: space-around;
}
</style>

<div class="card" style="{background}">
    <div class="content">
        <h3>{header}</h3>
        <p>{text}</p>
    </div>
    <div class="img-wrapper">
        <img src="{imgUrl}" alt="{imgAlt}">
    </div>
</div>