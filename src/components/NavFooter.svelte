<nav aria-label="footer navigation">
  <ul class="navlist">
    <li class="navlist__item"><a href="/">About</a></li>
    <li class="navlist__item"><a href="/">Services</a></li>
    <li class="navlist__item"><a href="/">Projects</a></li>
  </ul>
</nav>

<style>
  .navlist {
    display: grid;
    grid-auto-flow: column;
    gap: 3.5625rem;
  }

  .navlist__item {
    color: var(--color-green);
    font-size: 1.125rem;
    line-height: 1.3889;
    letter-spacing: -0.0081rem;
    transition: color .4s ease;
  }

  .navlist__item:hover {
    color: var(--color-white);
  }
</style>