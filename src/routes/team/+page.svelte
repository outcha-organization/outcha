<script>
  import Header from "../Header.svelte";
  import Banner from "../Banner.svelte";
  import Footer from "../Footer.svelte";

  import banner from '$lib/images/team/banner.webp';
</script>

<svelte:head>
  <title>OUT'CHA - La Team</title>
  <meta name="description"
        content="Association qui a pour but de favoriser l'inclusion sociale et la réalisation de rêves par le sport." />
</svelte:head>

<Header />
<Banner title="La Team" image={banner} />

<div class="wrapper">
  <div class="container">
    <h2>L'équipe</h2>
    <p>
      Lorem ipsum dolor sit amet, consectetur adipisicing elit. Cumque doloremque exercitationem nesciunt omnis
      repellendus
      repudiandae rerum velit voluptate! Excepturi fuga libero magni obcaecati officia? Cumque dolorem iusto maxime quas
      quo.
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