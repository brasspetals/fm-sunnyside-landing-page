<script>
  import Link from './LinkUnderlined.svelte'
  export let card
</script>

<div class="pair">
  <div class="pair__img">
    <picture>
      <source srcset="{card.srcset}"
      media="{card.media}">
      <img src="{card.src}" alt="">
    </picture>
    
  </div>
  <div class="pair__text">
    <h2>{card.heading}</h2>
    <p>{card.description}</p>
    <Link color={card.color}/>
  </div>
</div>

<style>
  .pair {
    background-color: var(--color-white-bg);
  }

  .pair__text {
    padding: 4rem 1.5rem;
    display: grid;
    justify-items: center;
    text-align: center;
  }

  h2 {
    color: var(--color-dark-blue);
    font-size: 2rem;
    letter-spacing: -0.0144rem;
    margin-bottom: 1.5rem;
    line-height: 1.22;
    max-width: 16ch;
  }

  p {
    font-size: 1.125rem;
    font-weight: 600;
    letter-spacing: -0.0081rem;
    line-height: 1.667;
    margin-bottom: 2rem;
    max-width: 45ch;
  }

  img {
    width: 100%;
    display: block;
  }

  @media screen and (min-width: 750px) {
    .pair {
      display: grid;
      grid-auto-flow: column;
      grid-template-columns: 1fr 1fr;
      height: 28.125rem;
      overflow: hidden;
    }

    .pair__img {
      overflow: hidden;
    }

    img {
      height: 100%;
      object-fit: cover;
    }

    .pair__text {
      align-self: center;
      align-content: center;
      justify-content: center;
      padding: 4rem 2.5rem;
    }

    p {
      max-width: 37ch;
    }
  }

  @media only screen and (min-width: 1000px) {
    .pair {
      height: 37.5rem;
    }

    .pair__text {
      text-align: left;
      justify-items: left;
    }

    h2 {
      font-size: 2.5rem;
      letter-spacing: -0.0181rem;
      margin-bottom: 2rem;
      max-width: 15ch;
    }

    p {
      margin-bottom: 2.5rem;
      max-width: 44ch;
    }

    :global(.pair__text a) {
      margin-left: 0.5625rem;
    }
    
  }
</style>