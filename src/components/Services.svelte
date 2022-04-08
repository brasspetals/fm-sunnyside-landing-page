<script>
  import Card from "./CardSingle.svelte"
  import {cardSingles as services} from '../../public/scripts/cardSingles.js'
</script>

<section class="services">
  {#each services as service}
    <Card card={service}/>
  {/each}
</section>