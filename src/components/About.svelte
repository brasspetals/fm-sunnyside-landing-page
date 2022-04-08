<script>
  import {cardPairs as cards} from '../../public/scripts/cardPairs.js'
  import CardPair from './CardPair.svelte'
</script>

<section class="about">
 {#each cards as card}
  <CardPair card={card}/>
 {/each}
</section>