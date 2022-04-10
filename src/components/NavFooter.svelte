<nav aria-label="footer navigation">
  <ul class="footer-nav">
    <li class="footer-nav__item"><a href="/">About</a></li>
    <li class="footer-nav__item"><a href="/">Services</a></li>
    <li class="footer-nav__item"><a href="/">Projects</a></li>
  </ul>
</nav>

<style>
  .footer-nav {
    display: grid;
    grid-auto-flow: column;
    gap: 3.5625rem;
  }

  .footer-nav__item {
    color: var(--color-green);
    font-size: 1.125rem;
    line-height: 1.3889;
    letter-spacing: -0.0081rem;
    transition: color .2s ease;
  }

  .footer-nav__item a:focus-visible {
    outline: 0.1875rem dashed var(--color-white);
    outline-offset: 0.3125rem;
  }

  .footer-nav__item:hover {
    color: var(--color-white);
  }
</style>