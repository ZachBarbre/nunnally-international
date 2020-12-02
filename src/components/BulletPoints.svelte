<script>
    export let content;
</script>

<style>
    section {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }

    h2 {
        margin: 5rem 0 2rem 0;
        text-align: center;
    }
    .point-container {
        width: 75%;
        display: flex;
        justify-content: space-around;
        align-items: stretch;
        flex-flow: row wrap;
    }
    .img-wrapper {
        width: 60px;
        height: 60px;
    }
    img {
        width: 100%;
        height: 100%;
    }
    .point {
        flex: 0 1 240px;
        display: flex;
        flex-direction: column;
        align-items: center;
        background: #FFF;
        padding: 4% 2%;
        margin: 5% 0;
    }

    h3 {
        padding: 1.5rem 0 1rem 0;
        font-size: 1.4rem;
    }

    p {
        text-align: center;
    }
</style>

<section style="{content.background}">
    {#if content.title}
        <h2>{content.title}</h2>
    {/if}
    <slot></slot>
    <div class="point-container">
        {#each content.points as point}
            <div class="point" style="{content.width}">
                {#if point.img}
                    <div class="img-wrapper">
                        <img src="{point.img}" alt="{point.imgAlt}">
                    </div>
                {/if}
                <h3>{point.header}</h3>
                {#each point.text as pointText}
                    <p>{pointText}</p>
                {/each}
            </div>
        {/each}
    </div>
</section>