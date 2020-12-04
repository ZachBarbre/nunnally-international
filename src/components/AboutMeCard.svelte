<script>
    export let content;
    const { imgUrl, imgAlt, text, header, background, isFipped } = content;
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
    justify-content: space-around;
    align-items: center;
}

.img-wrapper {
    /* height: 35vh; */
    flex: 0 1 510px;
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
    /* margin: 1.5rem 0; */
    padding: 1.5rem;
}

.content p {
    font-size: 18px;
    /* text-align: center; */
}

.wrapper {
    margin: 0 auto;
    display: flex;
    flex-direction: column;
    align-items: center;
    max-width: 1660px;
}

@media (max-width: 1000px) {
    section {
        width: 100%;
    }
}

</style>

<section style="{background}">
    <div class="wrapper">
        <div class="card">
            {#if isFipped}            
                <div class="content" style="{background.includes('url') ? 'background: #FFF' : ''}">
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
                <div class="content" style="{background.includes('url') ? 'background: #FFF' : ''}">
                    <h3>{header}</h3>
                    <p>{text}</p>
                    <slot name="side"></slot>
                </div>
            {/if}
            <slot name="under"></slot>
        </div>
    </div>
</section>