<script>
  import sandrine from '$lib/images/home/projects/sandrine.webp';
  import lapland from '$lib/images/home/projects/lapland.webp';
  import grandToGrand from '$lib/images/home/projects/grand-to-grand.webp';
  import Icon from "@iconify/svelte";
</script>

<section class="wrapper">
  <div class="container">
    <h1><em>Projets</em> OUT'CHA</h1>

    <div class="projects">
      <a href="/projets/sandrine" class="card">
        <div class="card-image">
          <img src={sandrine} alt="Sandrine" />
        </div>
        <div class="card-content">
          <h2 class="title">Sandrine</h2>
          <h3 class="subtitle">Courir Sierre-Zinal en étant aveugle</h3>
        </div>
      </a>

      <a href="/projets/laponie" class="card">
        <div class="card-image">
          <img src="{lapland}" alt="Laponie" />
        </div>
        <div class="card-content">
          <h2 class="title">Laponie</h2>
          <h3 class="subtitle">La revanche du Grand Nord</h3>
        </div>
      </a>

      <a href="/projets/grand-to-grand" class="card">
        <div class="card-image">
          <img src="{grandToGrand}" alt="Grand to Grand">
        </div>
        <div class="card-content">
          <h2 class="title">Grand to Grand</h2>
          <h3 class="subtitle">Un ultra-trail de 270 km en Utah</h3>
        </div>
      </a>
    </div>

    <div class="more">
      <a href="/projets" class="button">
        Voir tous les projets
        <span class="icon"><Icon icon="material-symbols:arrow-forward-ios" /></span>
      </a>
    </div>
  </div>
</section>

<style lang="sass">
  @use '$lib/sass/utilities/variables' as *
  @use '$lib/sass/utilities/mixins' as *

  .wrapper
    background-image: url("../../../lib/images/bg-green-dots.jpg")
    background-size: cover
    margin: 40px 0

  h1
    font-family: 'Anton', sans-serif
    font-weight: 400
    font-size: 60px
    text-transform: uppercase
    line-height: 1
    margin: 24px 0

    em
      font-family: 'Great Sejagad', sans-serif
      color: $primary
      display: block
      font-size: 32px
      font-weight: 400
      line-height: 1
      position: relative

  .projects
    display: flex
    justify-content: space-between
    align-items: center
    flex-direction: column
    gap: 30px

    +tablet
      flex-direction: row

  .card
    width: 100%
    height: 320px
    overflow: hidden
    position: relative
    max-width: 450px

    &:hover img
      transform: scale(1.1)

  .card-image
    width: 100%
    height: 100%
    position: absolute

    img
      width: 100%
      height: 100%
      object-fit: cover
      transition: 0.7s

  .card-content
    top: 0
    bottom: 0
    position: absolute
    display: flex
    flex-direction: column
    justify-content: flex-end
    color: #fff
    padding: 16px

    .title
      font-family: 'Anton', sans-serif
      text-transform: uppercase
      text-shadow: 1px 1px 4px #333
      font-size: 40px
      margin: 0

    .subtitle
      text-shadow: 1px 1px 4px #333
      font-size: 22px
      margin: 0

  .more
    text-align: center
    padding: 20px 0
</style>