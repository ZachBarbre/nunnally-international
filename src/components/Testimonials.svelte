<script>
  export let content;

  const testimonialArray = content.slice(0,2)
</script>

<style>
 section {
  background-color: #A57F60;
 }

 
</style>

<section>
  <h3></h3>
  {#each testimonialArray as testimonial}
    <div>
      
    </div>
  {/each}
</section>