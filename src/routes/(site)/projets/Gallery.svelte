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
  @use '$lib/sass/utilities/mixins' as *

  h2
    font-family: 'Anton', sans-serif
    text-transform: uppercase
    font-size: 24px
    letter-spacing: 1px
    line-height: 70px
    margin: 0

  #gallery
    display: grid
    grid-template-columns: 1fr 1fr
    gap: 15px
    margin-bottom: 20px

    a
      margin: 0 auto
      background-color: #001
      width: 100%

    img
      margin: 0 auto
      max-width: 100%
      display: block
      overflow: hidden
      object-fit: cover
      height: 174px
      width: 100%

      +tablet
        height: 90px

      +desktop
        height: 103px
</style>