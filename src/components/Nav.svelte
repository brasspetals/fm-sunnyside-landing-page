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
    <li class="menu-item"><a href="/">About</a></li>
    <li class="menu-item"><a href="/">Services</a></li>
    <li class="menu-item"><a href="/">Projects</a></li>
    <li class="menu-contact"><a href="/">Contact</a></li>
  </ul>
</nav>

<style>
  button {
    transition: opacity .4s ease;
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
    max-width: 31.25rem;
    display: grid;
    justify-items: center;
    grid-gap: 2rem;
    padding: 2.5rem 0;
    background-color: var(--color-white);
    transition: all .3s ease;
  }

  .menu::before {
    position: absolute;
    content: "";
    top: -1.5rem;
    right: 0;
    border: .75rem solid;
    border-color: transparent var(--color-white) var(--color-white)transparent;
  }

  .menu-item {
    color: var(--color-gray-blue);
    font-weight: 600;
    font-size: 1.25rem;
    line-height: 1.25;
    letter-spacing: -0.0088rem;
  }

  .menu-contact {
    color: var(--color-dark-blue);
    text-transform: uppercase;
    font-family: "Fraunces", serif;
    font-weight: 700;
    font-size: 0.9375rem;
    line-height: 1.667;
    background-color: var(--color-yellow);
    border-radius: 2rem;
    padding: 1rem 2rem;
  } 
</style>