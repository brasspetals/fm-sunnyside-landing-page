<script>
  import { fade, fly } from 'svelte/transition';
  import ContactBtn from './ContactBtn.svelte'

  let width
  let active = false;
  
  function toggleMenu(state) {
    active = typeof state === 'boolean' ? state : !active;
  }

</script>

<svelte:window bind:innerWidth={width}/>

<nav>
  <button aria-label="menu toggle" aria-expanded={active} class:open={active} on:click={toggleMenu}>
    <img src="/images/icon-hamburger.svg" alt="">
  </button>
  {#if active || width >= 800}
    <ul class="menu animate-none" transition:fade={{duration: 400}}>
      <li class="menu__item animate-none" in:fly={{duration: 500, y: -16, delay: 200}} out:fade><a href="/">About</a></li>
      <li class="menu__item animate-none" in:fly={{duration: 500, y: -16, delay:400}} out:fade><a href="/">Services</a></li>
      <li class="menu__item animate-none" in:fly={{duration: 500, y: -16, delay:600}} out:fade><a href="/">Projects</a></li>
      <li class="menu__contact animate-none" in:fly={{duration: 500, y: -16, delay:800}} out:fade>
        <ContactBtn/>
      </li>
    </ul>
  {/if}
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
    z-index: 2;
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

  @media screen and (min-width: 800px) {
    nav {
      margin-right: 0.4375rem;
    }

    button {
      display: none;
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

    .animate-none {
      animation-duration: 0.01ms !important;
      animation-iteration-count: 1 !important;
      transition-duration: 0.01ms !important;
      animation-delay: 0.01ms !important;
    }
  }
</style>