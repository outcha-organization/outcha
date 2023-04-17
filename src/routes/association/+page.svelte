<script>
  import Header from "../Header.svelte";
  import Banner from "../Banner.svelte";
  import Footer from "../Footer.svelte";

  import banner from '$lib/images/association/banner.webp';
  import Icon from '@iconify/svelte';
</script>

<svelte:head>
  <title>OUT'CHA - L'association</title>
  <meta name="description"
        content="Association qui a pour but de favoriser l'inclusion sociale et la réalisation de rêves par le sport." />
</svelte:head>

<Header />
<Banner title="L'association" image={banner} />

<div class="wrapper">
  <section class="about">
    <div class="container">
      <h1><em>Outdoor</em> Challenges</h1>
      <p>
        L’association a pour but de favoriser l’inclusion sociale,
        l’épanouissement, la réalisation de rêves et le partage par le sport,
        d’encourager la pratique du sport dans le respect de la nature,
        de promouvoir les échanges socio-culturels et l’intégration
        des valeurs sportives, chez les jeunes à travers le sport et les défis.
      </p>

      <p>
        <a href="/projets" class="button">
          Voir tous les projets
          <span class="icon"><Icon icon="material-symbols:arrow-forward-ios" /></span>
        </a>
      </p>

      <h2>Aidez nous</h2>
      <div class="card">
        <h3>Pour soutenir le projet:</h3>
        IBAN: CH53 0076 7000 S546 2495 4<br>
        Numéro TWINT : 078 958 06 26
      </div>
    </div>
  </section>
</div>

<Footer />

<style lang="sass">
  @use '../../lib/sass/variables' as *

  .wrapper
    background-color: #fff
    background-image: url("../../lib/images/bg-green-dots.jpg")
    background-size: cover
    padding: 30px 0
    min-height: 350px

  h1
    font-family: 'Anton', sans-serif
    font-weight: 400
    font-size: 55px
    text-transform: uppercase
    line-height: 1
    margin: 24px 0
    text-align: center

    em
      font-family: 'Great Sejagad', sans-serif
      color: $primary
      display: block
      font-size: 45px
      font-weight: 400
      line-height: .9
      position: relative

  h2
    font-family: 'Anton', sans-serif
    font-weight: 400
    font-size: 24px
    text-transform: uppercase
    line-height: 1
    margin: 0
    text-align: center

  h3
    margin: 12px 0

  .about
    padding-bottom: 30px

    p
      margin: 40px 0
      font-size: 18px
      font-weight: 500
      line-height: 30px
      text-align: center

    .card
      text-align: center
      line-height: 24px
</style>