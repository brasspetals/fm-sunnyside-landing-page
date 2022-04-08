<script>
  import Testimonial from "../Testimonial.svelte"
  import {testimonials} from "../../../public/scripts/testimonials"
</script>

<section class="client-testimonials">
  <h2>Client Testimonials</h2>
  <div class="testimonials">
    {#each testimonials as testimonial}
    <Testimonial testimonial={testimonial}/>
  {/each}
  </div>
</section>

<style>
  .client-testimonials {
    padding: 4rem 1.5rem 5.375rem;
    text-align: center;
  }

  h2 {
    font-size: 1rem;
    text-transform: uppercase;
    letter-spacing: 0.25rem;
    color: var(--color-gray);
    margin-bottom: 4rem;
  }

  .testimonials {
    display: grid;
    gap: 4rem;
  }
</style>