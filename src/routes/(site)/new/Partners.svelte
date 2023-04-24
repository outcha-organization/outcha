<script>
  import freudeHerrscht from '$lib/images/home/partners/freude-herrscht.png';
  import baechli from '$lib/images/home/partners/baechli.png';
  import maiday from '$lib/images/home/partners/maiday.png';
  import compex from '$lib/images/home/partners/compex.png';
  import bgcm from '$lib/images/home/partners/bgcm.png';
  import bonvin from '$lib/images/home/partners/bonvin.png';
  import bcv from '$lib/images/home/partners/bcv.png';
  import michot from '$lib/images/home/partners/michot.png';
</script>

<section class="wrapper">
  <div class="container">
    <ul class="partners">
      <li>
        <a href="https://www.freude-herrscht.ch/fran%C3%A7ais/" target="_blank">
          <img src="{freudeHerrscht}" alt="Freude herrscht" />
        </a>
      </li>
      <li>
        <a href="https://www.baechli-bergsport.ch/fr" target="_blank">
          <img src="{baechli}" alt="Bächli" />
        </a>
      </li>
      <li>
        <a href="https://maiday.ch/" target="_blank">
          <img src="{maiday}" alt="Maiday" />
        </a>
      </li>
      <li>
        <a href="https://www.compex.com/ch/fr/" target="_blank">
          <img src="{compex}" alt="Compex" />
        </a>
      </li>
      <li>
        <a href="https://bgcm.ch/" target="_blank">
          <img src="{bgcm}" alt="BGCM" />
        </a>
      </li>
      <li>
        <a href="https://bonvin1858.ch/" target="_blank">
          <img src="{bonvin}" alt="Bonvin" />
        </a>
      </li>
      <li>
        <a href="https://www.bcv.ch/" target="_blank">
          <img src="{bcv}" alt="BCV" />
        </a>
      </li>
      <li>
        <a href="http://eventente.ch/" target="_blank">
          <img src="{michot}" alt="Michot Eventente" />
        </a>
      </li>
    </ul>
  </div>
</section>

<style lang="sass">
  @use '../../../lib/sass/mixins' as *

  .partners
    list-style: none
    margin: 20px 0
    padding: 0
    display: grid
    grid-template-columns: 1fr 1fr 1fr 1fr
    gap: 15px

    li
      display: flex
      justify-content: center

    +tablet
      grid-template-columns: 1fr 1fr 1fr 1fr 1fr 1fr 1fr 1fr

    img
      max-width: 100%
      max-height: 100px
      display: block
</style>
