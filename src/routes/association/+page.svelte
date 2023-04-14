<script>
  import Header from "../Header.svelte";
  import Banner from "../Banner.svelte";
  import Footer from "../Footer.svelte";

  import banner from '$lib/images/association/banner.webp';
</script>

<svelte:head>
  <title>OUT'CHA - L'association</title>
  <meta name="description"
        content="Association qui a pour but de favoriser l'inclusion sociale et la réalisation de rêves par le sport." />
</svelte:head>

<Header />
<Banner title="L'association" image={banner} />

<div class="wrapper">
  <div class="container">
    <h2>Qui sommes-nous ?</h2>
    <p>
      L’association a pour but de favoriser l’inclusion sociale,
      l’épanouissement, la réalisation de rêves et le partage par le sport,
      d’encourager la pratique du sport dans le respect de la nature,
      de promouvoir les échanges socio-culturels et l’intégration
      des valeurs sportives, chez les jeunes à travers le sport et les défis.
    </p>
  </div>
</div>

<Footer />

<style lang="sass">
  .wrapper
    background-color: #fff
    padding: 30px 0
    min-height: 350px

  p
    margin: 0 0 15px 0
</style>