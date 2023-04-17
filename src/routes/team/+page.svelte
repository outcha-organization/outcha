<script>
  import Header from "../Header.svelte";
  import Banner from "../Banner.svelte";
  import Footer from "../Footer.svelte";

  import Icon from '@iconify/svelte';

  import banner from '$lib/images/team/banner.webp';
  import patrick from '$lib/images/team/Patrick Sumi.webp';
  import victor from '$lib/images/team/Victor Hugo Docarmo.webp';
  import herve from '$lib/images/team/Hervé Acosta.webp';
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
    <section class="person">
      <div class="picture">
        <img src={patrick} alt="Patrick Sumi" />
      </div>

      <div class="bio">
        <h3>Patrick Sumi</h3>
        <h4>49 ans, Lutry – Responsable de vente dans le secteur alimentaire</h4>
        <p>
          Pratique passionnément le sport depuis toujours grâce à son père qui a été son mentor.
          Ski de randonnée, trail, paddle, kayak et natation, rien ne lui échappe !
        </p>
        <p>
          En 2004, il se lance avec son ami Mike Boon dans le Tour du lac Léman en course à pied, un projet fou de 171
          km qu’ils accomplissent au bénéfice des enfants polyhandicapés.
          Ils récoltent plus de CHF 45'000.- de dons et créent l’association Just for Smiles qui est depuis devenue une
          fondation reconnue offrant des activités sportives aux enfants et adultes polyhandicapés.
        </p>
        <div class="perfs">
          <h5>
            <span class="icon"><Icon icon="ic:baseline-run-circle" /></span>
            Ses plus belles courses :
          </h5>
          <ul>
            <li>Le <strong>Grand to Grand</strong>, Arizona USA, 275 km par étape</li>
            <li>La <strong>PTL (UTMB)</strong>, 220 km</li>
            <li>La <strong>Patrouille des Glaciers</strong> (4x)</li>
            <li>La <strong>Pierra Menta</strong></li>
          </ul>
        </div>
      </div>
    </section>

    <section class="person">
      <div class="picture right">
        <img src={victor} alt="Victor Hugo Docarmo" />
      </div>

      <div class="bio">
        <h3>Victor Hugo Docarmo</h3>
        <h4>48 ans, Lausanne – Indépendant dans domaine dentaire</h4>
        <p>
          Né en Afrique, Victor déménage à Lisbonne avec ses frères où il vit pendant 10 ans.
          Il y pratique le football aux écoles du Sporting de Lisbonne.
          A l’âge de 12 ans, il rejoint ses parents en Suisse et une nouvelle aventure commence.
          Il intègre le club du Lausanne Sports où il effectuera tout son parcours de footballeur.
          Pratiquant assidument le ski alpinisme et la course à pied, cet amoureux de la montagne et de la nature se
          tourne ensuite naturellement vers les courses de trail et ultra trail avec un terrain de prédilection, les
          alpes
          vaudoises.
        </p>
        <div class="perfs">
          <h5>
            <span class="icon"><Icon icon="ic:baseline-run-circle" /></span>
            Ses plus belles courses :
          </h5>
          <ul>
            <li>Le <strong>marathon des Sables</strong>, Maroc / 290 km</li>
            <li><strong>UTMB</strong>, France / 168 km / 10 000 m+</li>
            <li>La <strong>Diagonale des fous</strong>, La Réunion</li>
            <li>La <strong>Patrouille des glaciers</strong>, (2x)</li>
          </ul>
        </div>
      </div>
    </section>

    <section class="person">
      <div class="picture">
        <img src={herve} alt="Hervé Acosta" />
      </div>

      <div class="bio">
        <h3>Hervé Acosta</h3>
        <h4>45 ans, Bex – Responsable de vente dans le secteur vinicole</h4>
        <p>
          Né en Auvergne et de formation hôtelière, Hervé arrive en Suisse il y a 24 ans.
          Hervé est passionné de course à pied depuis son enfance... également de 2 CV et vieilles Citroën !
          Il s’entraine au <a href="https://www.footing-club.ch/" target="_blank">Footing Club de Lausanne</a> depuis de
          nombreuses années.
          Domicilié tout près de la montagne à Bex, le trail vient à lui tout naturellement, puis l’ultra trail.
        </p>
        <div class="perfs">
          <h5>
            <span class="icon"><Icon icon="ic:baseline-run-circle" /></span>
            Ses plus belles courses :
          </h5>
          <ul>
            <li>Le <strong>Marathon des Sables</strong>, Maroc, 290 km</li>
            <li>Le <strong>Grand to Grand</strong>, Arizona USA, 275 km par étape</li>
            <li>Plus d’une vingtaine de marathons</li>
            <li><strong>Glacier 3000 Run</strong></li>
          </ul>
        </div>
      </div>
    </section>
  </div>
</div>

<Footer />

<style lang="sass">
  @use '../../lib/sass/variables' as *
  @use '../../lib/sass/mixins' as *

  .wrapper
    background-color: #fff
    padding: 30px 0
    min-height: 350px

  p
    margin: 0 0 10px 0
    font-weight: 400
    line-height: 26px
    color: #1d1e21

  a
    color: #1d1e21
    transition: all 200ms ease

    &:hover
      color: $secondary

  .person
    display: flex
    flex-direction: column
    align-items: center
    column-gap: 50px
    row-gap: 20px
    margin: 20px 0
    font-size: 14px
    padding: 30px 0
    border-bottom: solid 1px #d2d2d2

    &:last-child
      border-bottom: none

    +tablet
      flex-direction: row

    .picture
      +tablet
        &.right
          order: 1

      img
        width: 350px

    .bio
      h3
        font-size: 32px
        margin: 0
        font-family: 'Anton', sans-serif
        font-weight: 400

      h4
        font-size: 18px
        margin: 0 0 15px 0

    .perfs
      h5
        font-size: 18px
        line-height: 34px
        margin: 5px 0
        font-family: 'Anton', sans-serif
        font-weight: 400

        .icon
          color: #e84f0c
          font-size: 34px
          vertical-align: middle
          margin-right: 5px

      ul
        margin: 0
        padding: 0 0 0 30px
        font-weight: 400
        line-height: 26px
        color: #1d1e21
</style>