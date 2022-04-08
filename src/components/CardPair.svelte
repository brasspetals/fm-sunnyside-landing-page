<script>
  import Link from './LinkUnderlined.svelte'
  export let card
</script>

<div class="pair">
  <div class="pair__img">
    <img srcset="{card.srcset}" alt="">
  </div>
  <div class="pair__text">
    <h2>{card.heading}</h2>
    <p>{card.description}</p>
    <Link color={card.color}/>
  </div>
</div>

<style>
  .pair {
    background-color: var(--color-white);
    text-align: center;
  }

  .pair__text {
    padding: 4rem 1.5rem;
    display: grid;
  }

  h2 {
    color: var(--color-dark-blue);
    font-size: 2rem;
    letter-spacing: -0.0144rem;
    margin-bottom: 1.5rem;
    line-height: 1.22
  }

  p {
    font-size: 1.125rem;
    font-weight: 600;
    letter-spacing: -0.0081rem;
    line-height: 1.667;
    margin-bottom: 2rem;
  }

  img {
    width: 100%;
    display: block;
  }
</style>