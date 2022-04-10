<script>import {cardPairs as cards} from '../../../public/scripts/cardPairs'
  
  import CardPair from '../CardPair.svelte'
</script>

<section class="about">
 {#each cards as card}
  <CardPair card={card}/>
 {/each}
</section>

<style>

  @media screen and (min-width: 750px) {
    :global(.pair:nth-of-type(odd) > .pair__img) {
      order: 2;
    }
  }

  @media screen and (min-width: 1325px) {
    :global(.pair:nth-of-type(odd) > .pair__text) {
      justify-content: right;
      padding-right: 6.5625rem;
    }

    :global(.pair:nth-of-type(even) > .pair__text) {
      justify-content: left;
      padding-left: 6.875rem;
    }
  }
</style>