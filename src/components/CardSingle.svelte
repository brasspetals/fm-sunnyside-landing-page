<script>
  export let card
</script>

<div class="service {card.type}">
  <div class="service__text">
    <h2>{card.heading}</h2>
    <p>{card.description}</p>
  </div>
</div>

<style>
  .service {
    background-size: cover;
    background-position: top center;
    background-repeat: no-repeat;
    height: 135vw;
    min-height: 37.5rem;
    text-align: center;
    display: grid;
    align-items: end;
  }

  .graphic-design {
    background-image: url('/images/mobile/image-graphic-design.jpg');
    color: var(--color-dark-green);
  }

  .photography {
    background-image: url('/images/mobile/image-photography.jpg');
    color: var(--color-blue);
  }

  .service__text {
    padding: 3.625rem 1.375rem;
  }

  h2 {
    text-transform: capitalize;
    margin-bottom: 1.75rem;
    font-size: 1.75rem;
    letter-spacing: -0.0125rem;
  }

  p {
    font-size: 1rem;
    line-height: 1.6875;
    letter-spacing: -0.0069rem;
    max-width: 50ch;
    margin: 0 auto;
  }

  @media screen and (min-width: 550px) {
    .service {
      height: 37.5rem;
      height: 40vw;
      max-height: 43.75rem;
    }

    .graphic-design {
      background-image: url('/images/desktop/image-graphic-design.jpg');
    }

    .photography {
      background-image: url('/images/desktop/image-photography.jpg');
    }
  }

  @media screen and (min-width: 750px) {
    p {
      max-width: 36ch;
    }
  }
</style>