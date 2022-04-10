<script>
  import Nav from '../Nav.svelte'
  import Logo from '../Logo.svelte'
</script>

<header>
  <div class="masthead">
    <Logo type="header"/>
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
    height: 140vw;
    max-height: 800px;
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

  @media screen and (min-width: 750px) {
    header {
      padding: 2.125rem 2.5rem;
      background-image: url('/images/desktop/image-header.jpg');
    }

    h1 {
      font-size: 3rem;
      letter-spacing: 0.5469rem;
      margin-top: 6.5625rem;
    }

    .hero img {
      margin-top: 5.75rem;
    }
  }

  @media screen and (min-width: 1000px) {
    h1 {
      font-size: 3.5rem;
    }
  }
</style>