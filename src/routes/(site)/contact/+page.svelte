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
    <h2>Contact</h2>
    <p>
      Lorem ipsum dolor sit amet, consectetur adipisicing elit. Cumque doloremque exercitationem nesciunt omnis
      repellendus
      repudiandae rerum velit voluptate! Excepturi fuga libero magni obcaecati officia? Cumque dolorem iusto maxime quas
      quo.
    </p>
  </div>
</div>

<style lang="sass">
  .wrapper
    background-color: #fff
    padding: 30px 0
    min-height: 350px

  p
    margin: 0 0 15px 0
</style>