<script>
  import '$lib/sass/global.sass'
  import Header from "./Header.svelte";
  import Footer from "./Footer.svelte";
</script>

<Header />
<slot />
<Footer />

<style lang="sass">
  @use '$lib/sass/utilities/mixins' as *

  :global(body)
    margin-top: 70px
    +tablet
      margin-top: 0
</style>