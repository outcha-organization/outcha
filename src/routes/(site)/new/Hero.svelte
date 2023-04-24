<script>
  import video from '$lib/videos/home-yukon.mp4';
  import Icon from '@iconify/svelte';
</script>

<section class="hero">
  <video
          class="hero-video"
          src="{video}"
          playsinline autoplay muted loop>
  </video>

  <div class="hero-content">
    <div class="container">
      <p class="subtitle">Outdoor</p>
      <p class="title">Challenges</p>
      <p class="tagline">Épanouissement, réalisation de rêves et partage par le sport</p>
      <p><a href="https://youtu.be/yLOG3ipbeNg" class="button" target="_blank">Découvrir l'association <span class="icon"><Icon icon="material-symbols:arrow-forward-ios" /></span></a></p>
    </div>
  </div>
</section>

<style lang="sass">
  @use '../../../lib/sass/variables' as *
  @use '../../../lib/sass/mixins' as *

  .hero
    position: relative
    display: grid
    place-items: center
    height: 65vh
    min-height: 450px
    width: 100%

    +tablet
      min-height: 500px

  .hero-video
    position: absolute
    z-index: 0
    object-fit: cover
    width: 100%
    height: 100%

  .hero-content
    z-index: 1
    width: 100%
    height: 100%
    background: url("../../../lib/images/border-white-bottom.webp") repeat-x center bottom
    background-size: 100%
    display: flex
    justify-content: center
    text-align: center
    align-items: center

    +desktop
      text-align: left

  .title
    font-family: 'Anton', sans-serif
    font-weight: 400
    color: #fff
    font-size: 72px
    line-height: 72px
    letter-spacing: -1px
    text-transform: uppercase
    text-shadow: 2px 2px 6px #333
    margin: 0

    +tablet
      font-size: 85px
      line-height: 85px

  .subtitle
    font-family: 'Great Sejagad', sans-serif
    font-weight: 400
    font-size: 105px
    line-height: 60px
    color: $primary
    text-shadow: 1px 1px 6px #333
    margin: 0
    position: relative

    +tablet
      font-size: 120px
      line-height: 70px

  .tagline
    font-size: 26px
    color: #fff
    margin: 10px 0 30px 0
    text-shadow: 0 0 3px #999
</style>
