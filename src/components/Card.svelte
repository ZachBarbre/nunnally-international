<script>
    export let content;
    console.log(content)
    const { imgUrl, imgAlt, text, header, background, isFipped } = content;
    // console.log(imgUrl)
</script>

<style>
section {
    width: 80%;
    margin: 0 auto;
    padding: 5% 0;
}
.card {
    
    display: flex;
    flex-flow: row wrap;
    justify-content: space-around;
}

.img-wrapper {
    height: 40vh;
    flex: 0 1 400px;
}

img {
    height: 100%;
    width: 100%;
}

.content {
    flex: 0 1 400px;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    margin: 1.5rem 0;
}

.content p {
    font-size: 18px;
    text-align: center;
}

@media (max-width: 1000px) {
    section {
        width: 100%;
    }
}

</style>

<section style="{background}">
    <div class="card">
        {#if isFipped}            
        <div class="content">
            <h3>{header}</h3>   
            <p>{text}</p>
            <slot></slot>
        </div>
        <div class="img-wrapper">
            <img src="{imgUrl}" alt="{imgAlt}">
        </div>
        {:else}
        <div class="img-wrapper">
            <img src="{imgUrl}" alt="{imgAlt}">
        </div>
        <div class="content">
            <h3>{header}</h3>
            <p>{text}</p>
            <slot></slot>
        </div>
        {/if}
    </div>
</section>