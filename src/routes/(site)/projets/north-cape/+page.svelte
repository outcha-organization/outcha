<script>
  import Banner from '../../Banner.svelte';
  import Gallery from '../Gallery.svelte';

  import banner from '$lib/images/projets/bg-dark.webp';
  import Icon from '@iconify/svelte';

  import photo1 from '$lib/images/projets/north-cape/photo1.webp';
  import photo2 from '$lib/images/projets/north-cape/photo2.webp';
  import photo3 from '$lib/images/projets/north-cape/photo3.webp';
  import photo4 from '$lib/images/projets/north-cape/photo4.webp';

  const images = [
    { image: photo1, width: 960, height: 720 },
    { image: photo2, width: 1600, height: 1200 },
    { image: photo3, width: 1230, height: 2048 },
    { image: photo4, width: 1600, height: 1200 }
  ]
</script>

<svelte:head>
  <title>OUT'CHA - North Cape</title>
</svelte:head>

<Banner image={banner} />

<div class="wrapper">
  <div class="container">
    <div class="content">
      <nav class="breadcrumb">
        <ul>
          <li><a href="/projets">Projets</a></li>
          <li class="is-active"><a href="/projets/north-cape">North Cape</a></li>
        </ul>
      </nav>

      <div class="location">Norvège</div>
      <h1>North Cape</h1>
      <h3>5500 kilomètre à vélo jusqu'en Norvège</h3>
      <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Debitis deleniti dolorum exercitationem molestiae
        odio quisquam reprehenderit! A ad debitis eaque fugit harum illo laborum modi molestias officia praesentium,
        repudiandae suscipit?</p>
      <div class="cover">
        <img src={photo1} alt="North Cape" />
      </div>
      <article>
        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Debitis deleniti dolorum exercitationem molestiae
          odio quisquam reprehenderit! A ad debitis eaque fugit harum illo laborum modi molestias officia praesentium,
          repudiandae suscipit?</p>
        <img src={photo3} alt="North Cape" width="240" class="is-pulled-left" />
        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Debitis deleniti dolorum exercitationem molestiae
          odio quisquam reprehenderit! A ad debitis eaque fugit harum illo laborum modi molestias officia praesentium,
          repudiandae suscipit?</p>
        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Alias architecto at corporis, cum delectus deleniti
          dolor dolores ea eos expedita, explicabo facere magnam magni provident quia ratione rerum saepe
          voluptatibus?</p>
      </article>

      <p class="more">
        <a href="/projets">
          Voir les autres projets
          <span class="icon"><Icon icon="material-symbols:arrow-forward-ios" /></span>
        </a>
      </p>
    </div>

    <div class="sidebar">
      <Gallery images={images} />
    </div>
  </div>
</div>

<style lang="sass">
  @use '../../../../lib/sass/variables' as *
  @use '../../../../lib/sass/mixins' as *

  .wrapper
    background-color: #fff
    padding: 30px 0
    min-height: 350px

  .container
    display: flex
    flex-direction: column
    gap: 30px

    +tablet
      flex-direction: row

    +desktop
      gap: 50px

  .sidebar
    +tablet
      width: 700px
      padding-top: 60px

    +desktop
      width: 800px

  .location
    font-size: 24px

  h1
    font-family: 'Anton', sans-serif
    text-transform: uppercase
    font-size: 64px
    line-height: 90px
    margin: 0

    a
      color: #000
      text-decoration: none
      transition: 200ms ease

      &:hover
        color: $secondary

  h2
    font-family: 'Anton', sans-serif
    text-transform: uppercase
    font-size: 24px
    letter-spacing: 1px
    line-height: 70px
    margin: 0

  h3
    font-size: 24px
    margin: 0

  .cover
    margin: 20px 0

    img
      max-width: 100%

  p
    line-height: 24px

  article
    &::after
      clear: both
      content: " "
      display: table

    .is-pulled-left
      float: left
      margin-right: 20px

    .is-pulled-right
      float: right
      margin-left: 20px

  .more
    border-top: solid 1px $grey
    margin-top: 40px
    padding-top: 20px
    text-align: right

    a
      color: $tertiary
      text-decoration: none
      font-size: 18px
      font-weight: 600
      transition: all 200ms ease

      &:hover
        color: $secondary
        text-decoration: underline

      .icon
        font-size: 12px
</style>