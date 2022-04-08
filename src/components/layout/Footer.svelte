<script>
  import Logo from '../Logo.svelte'
  import NavFooter from '../NavFooter.svelte'
  import SocialLinks from '../SocialLinks.svelte'
</script>

<footer>
  <Logo type="footer"/>
  <NavFooter/>
  <SocialLinks/>
</footer>

<style>
  footer {
    padding: 4rem 2.4375rem;
    background-color: var(--color-light-green);
    display: grid;
    justify-content: center;
    justify-items: center;
  }
</style>