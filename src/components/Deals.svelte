<script>
  export let deals;
</script>

<div class="container">
  {#each deals.deals as deal}
    <div class="card">
      <div class="img-wrapper">
        <img src={deal.acquiredLogo} alt={deal.acquiredAlt} />
      </div>
      <p>
        {#if deal.acquiredByTextOveride}
          {deal.acquiredByTextOveride}
        {:else}
          has been acquired by
        {/if}
      </p>
      <div class="img-wrapper">
        <img src={deal.acquiredByLogo} alt={deal.acquiredByAlt} />
      </div>
      <p>{deal.acquiredText}</p>
      <p></p>
      <div class="img-wrapper">
        <img src="/logo.png" alt="Nunnally International Logo" />
      </div>
    </div>
  {/each}
</div>

<style>
  .container {
    margin: 0 auto;
    width: 85%;
    max-width: 1200px;
    display: flex;
    justify-content: space-around;
    align-items: stretch;
    flex-flow: row wrap;
  }

  .card {
    flex: 0 1 320px;
    padding: 1.5rem 2rem;
    margin: 2% 0;
    border: 1px solid #034078;
    border-radius: 2px;
    display: flex;
    flex-flow: column nowrap;
    justify-content: space-between;
    align-items: center;
  }

  .img-wrapper {
    min-width: 200px;
    max-width: 280px;
    position: relative;
    min-height: 158px;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  img {
    height: auto;
    width: 100%;
  }

  p {
    font-style: italic;
    text-align: center;
  }
</style>
