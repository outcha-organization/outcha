<script>
  export let title;
  export let image;

  import { onMount } from 'svelte';

  function parallaxEffect() {
    const distance = window.scrollY
    document.querySelector('.banner-img').style.transform = `translateY(${distance * 0.2}px)`
  }

  onMount(() => {
    window.addEventListener('scroll', parallaxEffect)
  });
</script>

<div class="banner" class:small={!title}>
  <div class="banner-img">
    <img src={image} alt={title} />
  </div>

  {#if title}
    <h1 class="title">{title}</h1>
  {/if}
</div>

<style lang="sass">
  @use '../lib/sass/mixins' as *

  .banner
    height: 260px
    display: flex
    justify-content: center
    align-items: center
    background: url("../lib/images/border-white-bottom.webp") repeat-x center bottom
    position: relative

    &.small
      height: 100px
      background-image: url("../lib/images/border-white-bottom-2.webp")
      background-size: cover

      img
        height: 120% !important

    +tablet
      height: 300px

    +desktop
      height: 350px

    .banner-img
      position: absolute
      top: 0
      left: 0
      width: 100%
      height: 100%
      object-fit: cover
      z-index: -1

      img
        position: absolute
        top: -20px
        left: 0
        width: 100%
        height: 106%
        object-fit: cover

    .title
      font-family: 'Great Sejagad', sans-serif
      margin: 0
      padding-top: 6px
      padding-bottom: 18px
      color: #fff
      font-size: 75px
      font-weight: 400
      z-index: 1

      +tablet
        font-size: 80px

      +desktop
        font-size: 90px
</style>
