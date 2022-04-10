<script>
  import Card from "../CardSingle.svelte"
  import {cardSingles as services} from '../../../public/scripts/cardSingles.js'
</script>

<section class="services">
  {#each services as service}
    <Card card={service}/>
  {/each}
</section>

<style>
  @media screen and (min-width: 750px) {
    .services {
      display: grid;
      grid-auto-flow: column;
      grid-template-columns: 1fr 1fr;
    }
  }
</style>