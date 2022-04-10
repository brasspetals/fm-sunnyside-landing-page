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
    background-color: var(--color-white-bg);
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

  @media screen and (min-width: 750px) {
    .client-testimonials {
      padding: 6rem 2.5rem;
    }

    h2 {
      font-size: 1.25rem;
      letter-spacing: 0.3125rem;
    }
  }

  @media screen and (min-width: 1150px) {
    .client-testimonials {
      padding: 10rem 2.5rem;
    }

    h2 {
      margin-bottom: 5rem;
    }

    .testimonials {
      grid-auto-flow: column;
      max-width: 69.375rem;
      margin: 0 auto;
      gap: 1.75rem;
    }
  }
</style>