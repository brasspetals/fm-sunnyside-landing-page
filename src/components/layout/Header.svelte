<script>
  import Nav from '../Nav.svelte'
  import Logo from '../Logo.svelte'
</script>

<header>
  <div class="masthead">
    <Logo/>
    <Nav/>
  </div>
  <div class="hero">
    <h1>We are creatives</h1>
    <img src="/images/icon-arrow-down.svg" alt="">
  </div>
</header>

<style>
  header {
    background-color:#3ebfff;
    background-image: url('/images/mobile/image-header.jpg');
    background-position: bottom center;
    background-size: cover;
    background-repeat: no-repeat;
    padding: 2rem 1.5rem;
    min-height: 33.625rem;
    position: relative;
  }

  .masthead {
    display: grid;
    grid-auto-flow: column;
    justify-content: space-between;
    align-items: center;
    position: relative;
  }

  .hero {
    text-align: center;
  }

  h1 {
    margin-top: 5.25rem;
    font-size: 2.5rem;
    letter-spacing: 0.3969rem;
    color: var(--color-white);
    text-transform: uppercase;
  }

  .hero img {
    margin-top: 3rem;
  }

</style>