<script>
  import '$lib/sass/global.sass'
  import Header from "./Header.svelte";
  import Footer from "./Footer.svelte";
</script>

<Header />
<slot />
<Footer />