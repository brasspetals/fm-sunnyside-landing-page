<script></script>

<a href="/">Contact</a>

<style>


  a {
    display: grid;
    justify-content: center;
    align-content: center;
    height: 3.5rem;
    width: 8.75rem;
    color: var(--color-dark-blue);
    text-transform: uppercase;
    font-family: "Fraunces", serif;
    font-weight: 700;
    font-size: 0.9375rem;
    line-height: 1.667;
    background-color: var(--color-yellow);
    border-radius: 2rem;
    cursor: pointer;
  } 

  a:focus-visible {
    outline: 0.1875rem dashed var(--color-gray-blue);
    outline-offset: 0.3125rem;
  }

  @media screen and (min-width: 800px) {
    a {
      background-color: var(--color-white);
      transition: color .2s ease, background-color .2s ease;
    }

    a:hover {
      background-color: hsla(0, 0%, 100%, 25%);
      color: var(--color-white);
    }

    a:focus-visible {
      outline: 0.1875rem dashed var(--color-white);
    }
  }

</style>