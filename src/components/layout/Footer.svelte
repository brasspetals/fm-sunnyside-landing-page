<script>
  import Logo from '../Logo.svelte'
  import NavFooter from '../NavFooter.svelte'
  import SocialLinks from '../SocialLinks.svelte'
  import Attribution from '../Attribution.svelte'
</script>

<footer>
  <Logo type="footer"/>
  <NavFooter/>
  <SocialLinks/>
  <Attribution/>
</footer>

<style>
  footer {
    padding: 4rem 2.4375rem 6rem;
    background-color: var(--color-light-green);
    display: grid;
    justify-content: center;
    justify-items: center;
    position: relative;
  }
</style>