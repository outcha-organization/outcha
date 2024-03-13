<script>
  import { onMount } from "svelte";
  import PhotoSwipeLightbox from 'photoswipe/lightbox';
  import 'photoswipe/style.css';
  import Banner from "../Banner.svelte";
  import banner from '$lib/images/projets/banner.webp';
  import Icon from "@iconify/svelte";

  import freudeHerrscht from '$lib/images/projets/freude-herrscht/photo1.webp';
  import freudeHerrscht2 from '$lib/images/projets/freude-herrscht/photo2.webp';
  import freudeHerrscht3 from '$lib/images/projets/freude-herrscht/photo3.webp';

  import afghansMontagne from '$lib/images/projets/afghans-montagne/photo1.webp';
  import afghansMontagne2 from '$lib/images/projets/afghans-montagne/photo2.webp';
  import afghansMontagne3 from '$lib/images/projets/afghans-montagne/photo3.webp';

  import sandrine from '$lib/images/projets/sandrine/photo1.webp';
  import sandrine2 from '$lib/images/projets/sandrine/photo2.webp';
  import sandrine3 from '$lib/images/projets/sandrine/photo3.webp';

  import afghansSki from '$lib/images/projets/afghans-ski/photo1.webp';
  import afghansSki2 from '$lib/images/projets/afghans-ski/photo2.webp';
  import afghansSki3 from '$lib/images/projets/afghans-ski/photo3.webp';

  onMount(() => {
    let lightbox = new PhotoSwipeLightbox({
      gallery: '.card-image',
      children: 'a',
      imageClickAction: 'close',
      tapAction: 'close',
      pswpModule: () => import('photoswipe'),
    });
    lightbox.init();
  })
</script>

<svelte:head>
  <title>OUT'CHA - Les projets</title>
  <meta name="description"
        content="Association qui a pour but de favoriser l'inclusion sociale et la réalisation de rêves par le sport." />
</svelte:head>

<Banner title="Les projets" image={banner} />

<div class="wrapper">
  <div class="container">
    <div class="projects">
      <div class="card" id="camps">
        <div class="card-image">
          <a href={freudeHerrscht} data-pswp-width="650" data-pswp-height="650">
            <img src={freudeHerrscht} alt="Freude Herrscht" />
          </a>
          <a href={freudeHerrscht2} data-pswp-width="650" data-pswp-height="650" style="display: none">
            <img src={freudeHerrscht2} alt="Freude Herrscht" />
          </a>
          <a href={freudeHerrscht3} data-pswp-width="650" data-pswp-height="650" style="display: none">
            <img src={freudeHerrscht3} alt="Freude Herrscht" />
          </a>
        </div>
        <div class="card-content">
          <h2><a href="/projets#camps">Camps d'activités</a></h2>
          <h3>en collaboration avec la Fondation Freude Herrscht</h3>
          <ul>
            <li>Des dixaines d’enfants dans le besoin peuvent partir à la montagne et profiter d’activité en plain air</li>
            <li>Une collaboration avec la Fondation Freude Herrscht</li>
            <li>Montant récolté et reversé à la Fondation >CHF 12’000.-</li>
          </ul>
        </div>
      </div>

      <div class="card" id="montagne">
        <div class="card-image">
          <a href={afghansMontagne} data-pswp-width="650" data-pswp-height="650">
            <img src={afghansMontagne} alt="WE à la montagne" />
          </a>
          <a href={afghansMontagne2} data-pswp-width="650" data-pswp-height="650" style="display: none">
            <img src={afghansMontagne2} alt="WE à la montagne" />
          </a>
          <a href={afghansMontagne3} data-pswp-width="650" data-pswp-height="650" style="display: none">
            <img src={afghansMontagne3} alt="WE à la montagne" />
          </a>
        </div>
        <div class="card-content">
          <h2><a href="/projets#montagne">Tour du Miroir d’Argentine</a></h2>
          <h3>avec cinq jeunes réfugiés Afghans</h3>
          <ul>
            <li>Grâce à Out’cha, Elham, Mohammad, Ramezan, Jawad et Layic ont pu profiter d’un week-end à la montagne et d’une nuit à l’alpage de la Vare</li>
            <li>Certains de ces Afghans ont traversés la Méditerranée en bateau gonflable!</li>
            <li>Budget pour cette activité >CHF 800.- (transports, repas, nuitées…)</li>
          </ul>
        </div>
      </div>

      <div class="card" id="sandrine">
        <div class="card-image">
          <a href={sandrine} data-pswp-width="650" data-pswp-height="650">
            <img src={sandrine} alt="Sandrine à Sierre-Zinal" />
          </a>
          <a href={sandrine2} data-pswp-width="650" data-pswp-height="650" style="display: none">
            <img src={sandrine3} alt="Sandrine à Sierre-Zinal" />
          </a>
          <a href={sandrine3} data-pswp-width="650" data-pswp-height="650" style="display: none">
            <img src={sandrine3} alt="Sandrine à Sierre-Zinal" />
          </a>
        </div>
        <div class="card-content">
          <h2><a href="/projets#sandrine">Sandrine à Sierre-Zinal</a></h2>
          <h3>le rêve de Sandrine Chauvy aveugle à 95%</h3>
          <ul>
            <li>Sandrine avait des rêves, participer et terminer Sierre-Zinal ainsi l’Ultracks de Zermatt</li>
            <li>Durant l’année 2022, l’équpie Out’cha s’est mobilisé pour entrainer, accompagner et motiver Sandrine afin qu’elle réalise ses rêves</li>
            <li>Budget pour cette activité >CHF 600.- (hotels, inscription, matériel…)</li>
          </ul>
        </div>
      </div>

      <div class="card" id="ski">
        <div class="card-image">
          <a href={afghansSki} data-pswp-width="650" data-pswp-height="650">
            <img src={afghansSki} alt="Ski de fond" />
          </a>
          <a href={afghansSki2} data-pswp-width="650" data-pswp-height="650" style="display: none">
            <img src={afghansSki2} alt="Ski de fond" />
          </a>
          <a href={afghansSki3} data-pswp-width="650" data-pswp-height="650" style="display: none">
            <img src={afghansSki3} alt="Ski de fond" />
          </a>
        </div>
        <div class="card-content">
          <h2><a href="/projets#ski">Ski de fond</a></h2>
          <h3>avec un Ukrainien et quatre jeunes réfugiés Afghans</h3>
          <ul>
            <li>Avec l’équipe Out’cha, Sardar, Yousef, Mehram, Hasmatullah et Mykola ont pu passer une journée aux Mosses pour tester les joies du ski de fond</li>
            <li>Joie, rire et expérience positives assurées</li>
            <li>Budget pour cette activité >CHF 500.- (transports, repas, location matériel…)</li>
          </ul>
        </div>
      </div>
    </div>

    <p class="has-text-centered">
      <a href="/association" class="button is-primary">
        <span>Soutenir l'association</span>
        <span class="icon">
          <Icon icon="material-symbols:arrow-forward-ios" />
        </span>
      </a>
    </p>
  </div>
</div>

<style lang="sass">
  .wrapper
    background-color: #fff
    background-size: cover
    padding: 30px 0
    min-height: 350px

  .projects
    margin-bottom: 20px

  .card
    display: flex
    flex-direction: column
    align-items: stretch
    gap: 30px
    border-bottom: solid 1px $grey
    padding: 30px 0

    +tablet
      flex-direction: row
      align-items: flex-start
      gap: 40px
      padding: 30px 20px

    +desktop
      padding: 40px

    .card-image
      a
        overflow: hidden
        position: relative
        display: block
        width: 100%
        max-width: 480px
        height: 280px
        margin: 0 auto

        +tablet
          width: 320px
          height: 240px

        img
          display: block
          width: 100%
          height: 100%
          object-fit: cover
          object-position: center center
          transition: 0.7s

          +tablet
            object-position: center

          &:hover
            transform: scale(1.1)

    .card-content
      padding: 0

      h2
        font-family: 'Anton', sans-serif
        text-transform: uppercase
        font-size: 40px
        line-height: 50px
        margin: 0

        a
          color: $primary
          text-decoration: none
          transition: color 200ms ease

          &:hover
            color: $primary-dark

      h3
        font-size: 22px
        margin: 0

      p
        line-height: 24px
        margin: 1rem 0

      ul
        list-style-type: disc
        margin: 20px 12px

      li
        margin: 12px
        line-height: 1.3

      a
        &.more
          color: $primary
          text-decoration: none
          transition: all 200ms ease

          &:hover
            color: $primary-dark
            text-decoration: underline

          .icon
            font-size: 12px
</style>