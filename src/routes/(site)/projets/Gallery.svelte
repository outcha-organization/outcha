<script>
  import { onMount } from "svelte";
  import PhotoSwipeLightbox from 'photoswipe/lightbox';
  import 'photoswipe/style.css';

  export let title = 'Galerie';
  export let images;

  onMount(() => {
    let lightbox = new PhotoSwipeLightbox({
      gallery: '#gallery',
      children: 'a',
      imageClickAction: 'close',
      tapAction: 'close',
      pswpModule: () => import('photoswipe'),
    });
    lightbox.init();
  })
</script>

<h2>{title}</h2>
<div id="gallery">
  {#each images as image, i}
    <a
      href={image.image}
      data-pswp-width={image.width}
      data-pswp-height={image.height}
    >
      <img src={image.image} alt="Photo {i + 1}" />
    </a>
  {/each}
</div>

<style lang="sass">
  @use '../../../lib/sass/mixins' as *

  h2
    font-family: 'Anton', sans-serif
    text-transform: uppercase
    font-size: 24px
    letter-spacing: 1px
    line-height: 70px
    margin: 0

  #gallery
    display: grid
    grid-template-columns: 1fr 1fr 1fr
    gap: 15px
    margin-bottom: 20px

    +tablet
      grid-template-columns: 1fr 1fr

    img
      max-width: 100%
      display: block
      overflow: hidden
      object-fit: cover
      width: 232px
      height: 174px

      +tablet
        width: 137px
        height: 103px
</style>