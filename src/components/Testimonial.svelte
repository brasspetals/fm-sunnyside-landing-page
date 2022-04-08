<script>
  export let testimonial
</script>

<div class="testimonial">
  <img src="{testimonial.avatar}" alt="" class="testimonial__avatar">
  <p class="testimonial__text">{testimonial.text}</p>
  <p class="testimonial__name">{testimonial.name}</p>
  <p class="testimonial__occupation">{testimonial.occupation}</p>
</div>

<style>
  .testimonial {
    display: grid;
    justify-content: center;
    justify-items: center;
  }

  .testimonial__avatar {
    border-radius: 50%;
    height: 4.5rem;
    width: auto;
    margin-bottom: 2rem;
    display: block;
  }

  .testimonial__text {
    font-size: 1.125rem;
    font-weight: 600;
    letter-spacing: -0.0081rem;
    line-height: 1.778;
    color: var(--color-dark-gray);
    margin-bottom: 2rem;
  }

  .testimonial__name {
    font-family: "Fraunces", serif;
    font-weight: 900;
    font-size: 1.125rem;
    letter-spacing: -0.0081rem;
    color: var(--color-dark-blue);
    margin-bottom: 0.5625rem;
  }

  .testimonial__occupation {
    color: var(--color-gray);
    text-transform: capitalize;
    font-size: 14px;
    line-height: 1.786;
    letter-spacing: -0.1px;
  }
</style>