<script>
  import freudeHerrscht from '$lib/images/home/projects/freude-herrscht.webp';
  import afghansMontagne from '$lib/images/home/projects/afghans-montagne.webp';
  import afghansSki from '$lib/images/home/projects/afghans-ski.webp';
  import sandrine from '$lib/images/home/projects/sandrine.webp';
  import Icon from "@iconify/svelte";
</script>

<section class="wrapper">
  <div class="container">
    <h1><em>Projets de</em> soutiens</h1>

    <div class="projects">
      <a href="/projets#camps" class="card">
        <div class="card-image">
          <img src="{freudeHerrscht}" alt="Freude Herrscht" />
        </div>
        <div class="card-content">
          <h2 class="title">Camps d'activités</h2>
          <h3 class="subtitle">avec Freude Herrscht</h3>
        </div>
      </a>

      <a href="/projets#montagne" class="card">
        <div class="card-image">
          <img src="{afghansMontagne}" alt="WE à la montagne">
        </div>
        <div class="card-content">
          <h2 class="title">Montagne</h2>
          <h3 class="subtitle">avec des réfugiés Afghans</h3>
        </div>
      </a>

      <a href="/projets#sandrine" class="card">
        <div class="card-image">
          <img src={sandrine} alt="Sandrine" />
        </div>
        <div class="card-content">
          <h2 class="title">Sandrine</h2>
          <h3 class="subtitle">Courir Sierre-Zinal en étant aveugle</h3>
        </div>
      </a>

      <a href="/projets#ski" class="card">
        <div class="card-image">
          <img src="{afghansSki}" alt="Ski de fond">
        </div>
        <div class="card-content">
          <h2 class="title">Ski de fond</h2>
          <h3 class="subtitle">avec des réfugiés Afghans</h3>
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
    height: 250px
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
      font-size: 25px
      margin: 0

    .subtitle
      text-shadow: 1px 1px 4px #333
      font-size: 22px
      margin: 0

  .more
    text-align: center
    padding: 20px 0
</style>