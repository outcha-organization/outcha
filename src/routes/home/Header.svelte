<script>
  import logo from '$lib/images/logo.webp';
  import Icon from '@iconify/svelte';
</script>

<div id="header">
  <h1 id="logo">
    <a href="/"><img src={logo} alt="Logo" /></a>
  </h1>

  <ul id="nav">
    <li><a href="/">Accueil</a></li>
    <li><a href="/about">L'association</a></li>
    <li><a href="/projects">Les projets</a></li>
    <li><a href="/team">La Team</a></li>
    <li><a href="/contact">Contact</a></li>
  </ul>

  <div id="nav-toggler">
    <button>
      <Icon icon="icon-park-outline:hamburger-button" />
    </button>
  </div>
</div>

<style lang="sass">
  @use '../../lib/sass/mixins' as *

  #header
    background-color: #fff
    display: flex
    align-items: center
    justify-content: center
    position: fixed
    top: 0
    left: 0
    right: 0
    height: 70px
    z-index: 2

    +tablet
      position: static
      padding: 0 4%
      height: 90px
      justify-content: space-between

    +desktop
      height: 100px

  #logo
    margin: 0

    img
      height: 75px

      +tablet
        height: 75px

      +desktop
        height: 90px

  #nav
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

  #nav-toggler
    display: flex
    justify-content: flex-end
    align-items: center
    position: absolute
    top: 0
    left: 0
    right: 0
    height: 70px
    padding: 0 20px

    button
      display: flex
      justify-content: center
      align-items: center
      padding: 0
      color: #000
      font-size: 32px
      background-color: transparent
      border: 0
      border-radius: 4px
      height: 45px
      width: 45px
      text-align: center
      cursor: pointer

      &:hover
        background-color: #fafafa

    +tablet
      display: none
</style>