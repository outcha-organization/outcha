<script>
  import Banner from "../Banner.svelte";
  import banner from '$lib/images/contact/banner.webp';
</script>

<svelte:head>
  <title>OUT'CHA - Contact</title>
  <meta name="description"
        content="Association qui a pour but de favoriser l'inclusion sociale et la réalisation de rêves par le sport." />
</svelte:head>

<Banner title="Contact" image={banner} />

<div class="wrapper">
  <div class="container">
    <div class="columns gap-6">
      <div class="column">
        <h1>Nous contacter</h1>
        <p><strong>L'association OUT'CHA est basée à Lausanne</strong></p>
        <p>
          C/o Oral design int<br>
          Rue Centrale 6<br>
          1003 Lausanne, Suisse
        </p>
        <p><a href="mailto:info@outcha.org" class="button is-small">info@outcha.org</a></p>
      </div>
      <div class="column">
        <h2>Nous soutenir</h2>
        <p>
          IBAN: CH53 0076 7000 S546 2495 4<br>
          Numéro TWINT : 078 958 06 26
        </p>
        <p class="mb-5"><small>Attestation de don sur demande</small></p>

        <h3>Par téléphone:</h3>
        Hervé: 078 858 58 69 / Victor: 079 212 59 66
      </div>
    </div>
  </div>
</div>

<style lang="sass">
  .wrapper
    background-color: #fff
    padding: 30px 0
    min-height: 350px
    text-align: center

  h1
    font-family: 'Anton', sans-serif
    font-weight: 400
    font-size: 32px
    text-transform: uppercase
    margin-bottom: 24px

  h2
    font-family: 'Anton', sans-serif
    font-weight: 400
    font-size: 24px
    text-transform: uppercase
    margin-bottom: 24px

  h3
    font-weight: 600
    font-size: 16px
    margin-bottom: 10px

  p
    font-weight: 400
    line-height: 24px
    margin-bottom: 16px
</style>