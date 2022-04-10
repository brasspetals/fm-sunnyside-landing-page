<script>
  let active = false;
  function toggleMenu(state) {
    active = typeof state === 'boolean' ? state : !active;
  }

</script>

<nav>
  <button aria-label="menu toggle" aria-expanded={active} class:open={active} on:click={toggleMenu}>
    <img src="/images/icon-hamburger.svg" alt="">
  </button>
  <ul class="menu" class:closed={!active}>
    <li class="menu__item"><a href="/">About</a></li>
    <li class="menu__item"><a href="/">Services</a></li>
    <li class="menu__item"><a href="/">Projects</a></li>
    <li class="menu__contact"><a href="/">Contact</a></li>
  </ul>
</nav>

<style>
  button {
    transition: opacity .4s ease;
  }

  button:focus-visible {
    outline: 0.1875rem dashed var(--color-white);
    outline-offset: 0.3125rem;
  }

  .open {
    opacity: 0.6;
  }

  .closed {
    opacity: 0;
    visibility: hidden;
  }

  .menu {
    position: absolute;
    top: 4.625rem;
    right: 0;
    width: 100%;
    display: grid;
    justify-items: center;
    grid-gap: 2rem;
    padding: 2.5rem 0;
    background-color: #FFFCF8;
    transition: all .3s ease;
  }

  .menu::before {
    position: absolute;
    content: "";
    top: -1.5rem;
    right: 0;
    border: .75rem solid;
    border-color: transparent #FFFCF8 #FFFCF8 transparent;
  }

  .menu__item {
    color: var(--color-gray-blue);
    font-weight: 600;
    font-size: 1.25rem;
    line-height: 1.25;
    letter-spacing: -0.0088rem;
  }

  .menu__item a:focus-visible {
    outline: 0.1875rem dashed var(--color-gray-blue);
    outline-offset: 0.3125rem;
  }

  .menu__contact a {
    color: var(--color-dark-blue);
    text-transform: uppercase;
    font-family: "Fraunces", serif;
    font-weight: 700;
    font-size: 0.9375rem;
    line-height: 1.667;
    background-color: var(--color-yellow);
    border-radius: 2rem;
    padding: 1rem 2rem;
    cursor: pointer;
  } 

  .menu__contact a:focus-visible {
      outline: 0.1875rem dashed var(--color-gray-blue);
      outline-offset: 0.3125rem;
    }

  @media screen and (min-width: 800px) {
    nav {
      margin-right: 0.4375rem;
    }

    button {
      display: none;
    }

    .closed {
      opacity: 1;
      visibility: visible;
    }

    .menu {
      background-color: unset;
      position: relative;
      top: unset;
      right: unset;
      grid-auto-flow: column;
      align-items: center;
      padding: unset;
      gap: 3rem;
    }

    .menu::before {
      display: none;
    }

    .menu__item {
      color: var(--color-white);
      font-size: 1.125rem;
      line-height: 1.3889;
      letter-spacing: -0.0081rem;
    }

    .menu__item a:focus-visible {
      outline: 0.1875rem dashed var(--color-white);
    }

    .menu__contact a {
      background-color: var(--color-white);
      transition: color .2s ease, background-color .2s ease;
    }

    .menu__contact a:hover {
      background-color: hsla(0, 0%, 100%, 25%);
      color: var(--color-white);
    }

    .menu__contact a:focus-visible {
      outline: 0.1875rem dashed var(--color-white);
    }
  }
</style>