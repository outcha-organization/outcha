<script>
  import { fade } from 'svelte/transition';

  import logo from '$lib/images/logo.webp';
  import Icon from '@iconify/svelte';

  let showNav = false;

  function toggleNav() {
    showNav = !showNav;
  }
</script>

<div id="header">
  <h1 id="logo">
    <a href="/"><img src={logo} alt="Logo" /></a>
  </h1>

  <ul id="nav" class:visible={showNav}>
    <li><a href="/">Accueil</a></li>
    <li><a href="/about">L'association</a></li>
    <li><a href="/projects">Les projets</a></li>
    <li><a href="/team">La Team</a></li>
    <li><a href="/contact">Contact</a></li>
  </ul>

  <div id="nav-toggler">
    <button on:click={toggleNav}>
      <Icon icon="icon-park-outline:hamburger-button" />
    </button>
  </div>
</div>

{#if showNav}
  <div class="backdrop" on:click={toggleNav} transition:fade="{{ duration: 200 }}"></div>
{/if}

<style lang="sass">
  @use '../../lib/sass/mixins' as *

  #header
    background-color: #fff
    position: fixed
    top: 0
    left: 0
    right: 0
    height: 70px
    z-index: 3

    +tablet
      position: static
      padding: 0 4%
      display: flex
      flex-direction: row
      justify-content: space-between
      height: 90px

    +desktop
      height: 100px

  #logo
    margin: 0
    display: flex
    justify-content: center
    position: relative
    z-index: 3

    img
      height: 70px
      display: block

      +tablet
        height: 75px

      +desktop
        height: 90px

  #nav
    list-style: none
    margin: 0
    padding: 20px 0
    background-color: #fff
    display: flex
    flex-direction: column
    align-items: center
    position: relative
    top: 0
    transform: translateY(-100%)
    transition: transform 0.3s ease-in-out

    +tablet
      position: static
      padding: 0
      flex-direction: row
      transform: translateY(0)

    &.visible
      transform: translateY(0)

    li
      padding: 2px 10px
      font-size: 16px
      letter-spacing: -1px

      +desktop
        font-size: 18px
        padding: 0 12px

    a
      text-decoration: none
      color: #333
      text-transform: uppercase
      line-height: 40px
      display: block
      padding: 10px 30px
      font-weight: 600

      +tablet
        font-weight: normal
        padding: 0
        border-bottom: 2px solid transparent

        &:hover
          border-bottom: 2px solid #ff1130

        &.router-link-active
          border-bottom: 2px solid #ff1130
          color: #ff1130

  #nav-toggler
    position: absolute
    top: 0
    right: 0
    padding: 12px 20px 13px 20px
    z-index: 3

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

  .backdrop
    position: fixed
    top: 0
    left: 0
    z-index: 2
    width: 100vw
    height: 100vh
    background-color: #000
    opacity: 0.5

    +tablet
      display: none
</style>