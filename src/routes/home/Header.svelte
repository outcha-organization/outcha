<script>
  import logo from '$lib/images/logo.jpg';
</script>

<div class="header">
  <h1 class="logo">
    <a href="/"><img src={logo} alt="Logo" /></a>
  </h1>

  <ul class="nav">
    <li><a href="/">Accueil</a></li>
    <li><a href="/about">L'association</a></li>
    <li><a href="/projects">Les projets</a></li>
    <li><a href="/team">La Team</a></li>
    <li><a href="/contact">Contact</a></li>
  </ul>
</div>

<style lang="sass">
  @use '../../lib/sass/mixins' as *

  .header
    background-color: #fff
    display: flex
    align-items: center
    padding: 15px 0 5px 0
    justify-content: center

    +tablet
      padding: 25px 4% 10px 4%
      justify-content: space-between

    +desktop
      padding: 25px 45px 10px 45px

  .logo
    margin: 0

    img
      height: 55px

      +tablet
        height: 55px

      +desktop
        height: 70px

  .nav
    list-style: none
    margin: 0
    padding: 0
    display: none

    +tablet
      display: flex

    li
      padding: 0 10px 10px 10px
      font-size: 16px
      letter-spacing: -1px

      +desktop
        font-size: 18px
        padding: 0 12px 12px 12px

    a
      text-decoration: none
      color: #333
      text-transform: uppercase
      line-height: 40px
      padding: 10px 0

      &:hover
        border-bottom: 2px solid #ff1130

      &.router-link-active
        border-bottom: 2px solid #ff1130
        color: #ff1130
</style>