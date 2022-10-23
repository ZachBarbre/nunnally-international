<script>
    export let content;
    const { imgUrl, imgAlt, text, header, background, isFipped, sideStyle } = content;
</script>

<style>
section {
    width: 85%;
    margin: 0 auto;
    padding: 4rem 0;
    background-size: cover;
}
.card {
    
    display: flex;
    flex-flow: row wrap;
    justify-content: space-between;
    align-items: center;
}

.img-wrapper {
    /* height: 35vh; */
    flex: 0 1 500px;
    min-width: 200px;
    position: relative;
    /* padding-left: 5px; */
}

img {
    height: auto;
    width: 100%;
}

.content {
    flex: 0 1 500px;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    /* padding: 0 1.5rem; */
}

.content p {
    font-size: 18px;
}

.wrapper {
    margin: 0 auto;
    width: 80%;
    max-width: 1660px;
}

@media (max-width: 1024px) {
    section {
        width: 100%;
    }
    .card {
        flex-direction: column;
    }
    .content {
        flex: 0 1 auto;
    }
    .img-wrapper {
        flex: 0 1 auto;
    }
}
@media (max-width: 430px) {
    .content {
        padding: 0;
    }
}
</style>

<section style="{background}">
    <div class="wrapper">
        <div class="card">
            {#if isFipped}            
                <div class="content" style="{background.includes('url') ? 'background: #FFF' : ''} {sideStyle}">
                    <h3>{header}</h3>   
                    <p>{text}</p>
                    <slot name="side"></slot>
                </div>
                <div class="img-wrapper">
                    {#if imgUrl}
                        <img src="{imgUrl}" alt="{imgAlt}">
                    {/if}
                </div>
            {:else}
                <div class="img-wrapper">
                    {#if imgUrl}
                        <img src="{imgUrl}" alt="{imgAlt}">
                    {/if}
                </div>
                <div class="content" style="{background.includes('url') ? 'background: #FFF' : ''} {sideStyle}">
                    <h3>{header}</h3>
                    <p>{text}</p>
                    <slot name="side"></slot>
                </div>
            {/if}
            <slot name="under"></slot>
        </div>
    </div>
</section>