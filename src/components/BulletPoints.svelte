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
        width: 70%;
        display: flex;
        justify-content: space-around;
        align-items: center;
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
        flex: 0 1 220px;
        display: flex;
        flex-direction: column;
        align-items: center;
        background: #FFF;
        padding: 4% 2%;
        margin: 5% 0;
    }

    h4 {
        padding: 1.5rem 0 1rem 0;
        font-size: 1.4rem;
    }

    p {
        text-align: center;
    }
</style>

<section style="{content.background}">
    <h2>{content.title}</h2>
    <slot></slot>
    <div class="point-container">
        {#each content.points as point}
            <div class="point">
                <div class="img-wrapper">
                    <img src="{point.img}" alt="{point.imgAlt}">
                </div>
                <h4>{point.header}</h4>
                <p>{point.text}</p>
            </div>
        {/each}
    </div>
</section>