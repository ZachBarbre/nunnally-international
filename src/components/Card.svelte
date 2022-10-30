<script>
  export let content;
  const { imgUrl, imgAlt, text, header, background, isFipped, sideStyle } =
    content;
</script>

<section style={background}>
  <div class="wrapper">
    <div class="card">
      <div class="card-top">
        {#if isFipped}
          <div
            class="content"
            style="{background.includes('url')
              ? 'background: #FFF'
              : ''} {sideStyle}"
          >
            <h3>{header}</h3>
            <p>{text}</p>
            <slot name="side" />
          </div>
          <div class="img-wrapper">
            {#if imgUrl}
              <img src={imgUrl} alt={imgAlt} />
            {/if}
          </div>
        {:else}
          <div class="img-wrapper">
            {#if imgUrl}
              <img src={imgUrl} alt={imgAlt} />
            {/if}
          </div>
          <div
            class="content"
            style="{background.includes('url')
              ? 'background: #FFF'
              : ''} {sideStyle}"
          >
            <h3>{header}</h3>
            <p>{text}</p>
            <slot name="side" />
          </div>
        {/if}
      </div>
      <slot name="under" />
    </div>
  </div>
</section>

<style>
  section {
    width: 85%;
    margin: 0 auto;
    padding: 4rem 0;
    background-size: cover;
    max-width: 1920px;
  }
  /* .card {   
} */

  .card-top {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(450px, 1fr));
    justify-items: center;
    gap: 2rem;
  }

  .img-wrapper {
    flex: 0 1 500px;
    min-width: 200px;
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
    padding: 0 1.5rem;
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
  @media (max-width: 450px) {
    .card-top {
      grid-template-columns: unset;
    }
    .content {
      padding: 0;
    }
  }
</style>
