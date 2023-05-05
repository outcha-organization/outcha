<script>
  import '$lib/sass/global.sass'
  import Header from "./Header.svelte";
  import Footer from "./Footer.svelte";
</script>

<Header />
<slot />
<Footer />

<style lang="sass">
  :global(body)
    margin-top: 70px
    +tablet
      margin-top: 0
</style>