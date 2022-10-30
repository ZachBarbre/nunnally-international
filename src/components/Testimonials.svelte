<script>
  export let content;
  import Icon from "fa-svelte";
  import {
    faChevronRight,
    faChevronLeft,
  } from "@fortawesome/free-solid-svg-icons";

  let testimonialIndex = 0;
  $: testimonialArray = content.testimonials.slice(
    testimonialIndex,
    testimonialIndex + 2
  );
  function handleForward() {
    if (testimonialIndex + 2 < content.testimonials.length) {
      testimonialIndex += 2;
    }
  }
  function handleBack() {
    if (testimonialIndex - 2 >= 0) {
      testimonialIndex -= 2;
    }
  }
</script>

<section>
  <h2>{content.title}</h2>
  <div class="buttons">
    <button
      disabled={testimonialIndex === 0}
      on:click={handleBack}
      aria-label="Previous Testimonials"
      ><Icon icon={faChevronLeft} />
    </button>
    <button
      disabled={testimonialIndex + 2 >= content.testimonials.length}
      on:click={handleForward}
      aria-label="Next Testimonials"
      ><Icon icon={faChevronRight} />
    </button>
  </div>
  <div class="testimonial-container">
    {#each testimonialArray as testimonial}
      <div class="testimonial">
        <p>{testimonial.text}</p>
        <div class="client">
          <div class="dash">--</div>
          <div>
            <p class="name">{testimonial.name}</p>
            <p>{testimonial.title1}</p>
            <p>{testimonial.title2}</p>
          </div>
        </div>
      </div>
    {/each}
  </div>
</section>

<style>
  section {
    background-color: #fefcfb;
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 3rem 3rem 5rem;
    font-size: 18px;
  }

  h2 {
    margin: 2rem 0 1.5rem 0;
    text-align: center;
  }

  .buttons {
    margin: 0.5rem 0 1rem;
  }

  button {
    background: none;
    border: none;
    font-size: 18px;
    padding: 0.5rem;
  }

  button:hover {
    background: rgba(100, 100, 100, 0.1);
    border-radius: 5px 5px 5px 5px;
  }
  button:disabled {
    opacity: 0.75;
  }

  .testimonial-container {
    width: 75%;
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
    gap: 30px;
  }

  @media (max-width: 450px) {
    section {
      padding: 3rem 0 5rem;
    }
    .testimonial-container {
      grid-template-columns: unset;
    }
  }

  .testimonial {
    color: #fefcfb;
    background: rgba(3, 64, 120, 0.5);
    padding: 2rem;
    border-radius: 5px 5px 5px 5px;
  }

  .dash {
    margin-right: 0.5rem;
  }
  .client {
    display: flex;
    justify-content: flex-end;
  }

  .client p {
    margin: 0;
  }

  .name {
    font-weight: bold;
  }
</style>
