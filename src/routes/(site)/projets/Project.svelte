<script>
  import banner from '$lib/images/projets/bg-dark.webp';
  import Banner from '../Banner.svelte';
  import Icon from '@iconify/svelte';

  export let name;
</script>

<Banner image={banner} />

<div class="wrapper project">
  <div class="container">
    <div class="content">
      <nav class="breadcrumb">
        <ul>
          <li><a href="/projets">Projets</a></li>
          <li class="is-active"><a href="#">{name}</a></li>
        </ul>
      </nav>

      <slot name="content" />

      <p class="more">
        <a href="/projets">
          Voir les autres projets
          <span class="icon"><Icon icon="material-symbols:arrow-forward-ios" /></span>
        </a>
      </p>
    </div>

    <div class="sidebar">
      <slot name="sidebar" />
    </div>
  </div>
</div>

<style lang="sass">
  @use '$lib/sass/utilities/variables' as *
  @use '$lib/sass/utilities/mixins' as *

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

  .project
    :global(h1)
      font-family: 'Anton', sans-serif
      text-transform: uppercase
      font-size: 64px
      line-height: 65px
      margin: 10px 0

    :global(h2)
      font-size: 24px
      margin: 0 0 15px 0

    :global(h3)
      font-size: 18px
      margin: 0 0 15px 0

    :global(h4)
      font-size: 16px
      margin: 0 0 15px 0

    :global(p)
      margin: 15px 0
      line-height: 28px
      color: #333
</style>