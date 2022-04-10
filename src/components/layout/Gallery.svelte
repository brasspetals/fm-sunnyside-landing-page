<script>
  import {gallery} from '../../../public/scripts/gallery'
</script>

<div class="gallery">
  {#each gallery as image}
    <picture>
      <source srcset="{image.srcset}" media="{image.media}">
      <img src="{image.src}" alt="">
    </picture>
  {/each}
</div>

<style>
  .gallery {
    display: grid;
    grid-template-columns: 1fr 1fr;
  }

  .gallery img {
    width: 100%;
    display: block;
  }

  @media screen and (min-width: 750px) {
    .gallery {
      grid-template-columns: repeat(4, 1fr);
    }
  }
</style>