<script>
  import logo from '$lib/images/logo.webp';
</script>

<svelte:head>
  <title>OUT'CHA - Sport for all</title>
  <meta name="description" content="Association qui a pour but de favoriser l'inclusion sociale, l'épanouissement, la réalisation de rêves et le partage par le sport." />

  <style>
    body { margin: 0 !important; }
  </style>
</svelte:head>

<div class="container-full">
  <div class="hero">
    <div class="hero-head"></div>
    <div class="hero-content">
      <img src={logo} alt="Logo" class="logo" />
      <p>Nouveau site en construction</p>
      <a href="https://outcha.weebly.com" class="btn">
        Voir l'ancien site
      </a>
    </div>
    <div class="hero-foot"></div>
  </div>
</div>

<style lang="sass">
  @use '../lib/sass/mixins' as *

  .container-full
    background: url("../lib/images/background.webp") no-repeat center center / cover
    height: 100vh
    display: flex
    align-items: center

  .hero
    flex-grow: 1

  .hero-head
    background: url("../lib/images/border-white-bottom.webp") repeat-x bottom center
    height: 50px

  .hero-foot
    background: url("../lib/images/border-white-top.webp") repeat-x top center
    height: 50px

  .hero-content
    display: flex
    flex-direction: column
    justify-content: center
    align-items: center
    background-color: #fff
    padding: 20px 16px

    +tablet
      padding: 30px 24px

    +desktop
      padding: 40px 32px

    .logo
      width: 280px
      max-width: 100%
      max-height: 100%
      margin: 30px 0

      +tablet
        width: 380px

      +desktop
        width: 450px
        margin: 24px 0

    .btn
      background-color: #ddd
      color: #000
      padding: 12px 34px
      font-size: 18px
      font-weight: 600
      text-decoration: none
      transition: background-color 0.3s ease

      &:hover
        background-color: #fe0d2f
        color: #fff
</style>