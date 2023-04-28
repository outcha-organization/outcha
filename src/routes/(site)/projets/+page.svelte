<script>
  import Banner from "../Banner.svelte";
  import banner from '$lib/images/projets/banner.webp';
  import Icon from "@iconify/svelte";

  import northCape from "$lib/images/projets/north-cape.webp";
  import skiDeFond from "$lib/images/projets/ski-de-fond.webp";
  import lapland from "$lib/images/projets/lapland.webp";
  import sandrine from "$lib/images/projets/sandrine.webp";
  import yukon from "$lib/images/projets/yukon.webp";
  import grandToGrand from "$lib/images/projets/grand-to-grand.webp";
  import mds from "$lib/images/projets/mds.webp";
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
      <div class="card">
        <div class="card-image">
          <a href="/projets/north-cape"><img src={northCape} alt="North Cape" /></a>
        </div>
        <div class="card-content">
          <div class="location">Norvège</div>
          <h2><a href="/projets/north-cape">North Cape</a></h2>
          <h3>5500 kilomètre à vélo jusqu'en Norvège</h3>
          <p>
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. At consequuntur eaque enim labore modi nostrum
            odio perspiciatis quo repellendus tempore. Architecto assumenda earum ipsa nisi nulla perferendis quasi
            tempora vel!
          </p>
          <a href="/projets/north-cape" class="more">
            Lire la suite
            <span class="icon"><Icon icon="material-symbols:arrow-forward-ios" /></span>
          </a>
        </div>
      </div>

      <div class="card">
        <div class="card-image">
          <a href="/projets/ski-de-fond"><img src={skiDeFond} alt="Ski de fond" /></a>
        </div>
        <div class="card-content">
          <div class="location">Suisse</div>
          <h2><a href="/projets/ski-de-fond">Ski de fond</a></h2>
          <h3>Rencontre avec des réfugiés Afghans</h3>
          <p>
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Accusantium alias aliquam assumenda dolorem, eos
            error eum in maxime molestiae officia placeat porro quaerat quam, quibusdam quidem saepe vel vero. Sapiente!
          </p>
          <a href="/projets/ski-de-fond" class="more">
            Lire la suite
            <span class="icon"><Icon icon="material-symbols:arrow-forward-ios" /></span>
          </a>
        </div>
      </div>

      <div class="card">
        <div class="card-image">
          <a href="/projets/laponie"><img src="{lapland}" alt="Laponie" /></a>
        </div>
        <div class="card-content">
          <div class="location">Finlande</div>
          <h2><a href="/projets/laponie">Laponie</a></h2>
          <h3>La revanche du Grand Nord</h3>
          <p>
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Accusantium adipisci alias architecto aut deserunt
            dolor dolorem error et explicabo fugiat ipsum nam possimus, praesentium quibusdam, quis quos sequi similique
            voluptatibus?
          </p>
          <a href="/projets/laponie" class="more">
            Lire la suite
            <span class="icon"><Icon icon="material-symbols:arrow-forward-ios" /></span>
          </a>
        </div>
      </div>

      <div class="card">
        <div class="card-image">
          <a href="/projets/sandrine"><img src={sandrine} alt="Sandrine" /></a>
        </div>
        <div class="card-content">
          <div class="location">Suisse</div>
          <h2><a href="/projets/sandrine">Sandrine</a></h2>
          <h3>Courir Sierre-Zinal en étant aveugle</h3>
          <p>
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Accusantium alias aliquam assumenda dolorem, eos
            error eum in maxime molestiae officia placeat porro quaerat quam, quibusdam quidem saepe vel vero. Sapiente!
          </p>
          <a href="/projets/sandrine" class="more">
            Lire la suite
            <span class="icon"><Icon icon="material-symbols:arrow-forward-ios" /></span>
          </a>
        </div>
      </div>

      <div class="card">
        <div class="card-image">
          <a href="/projets/yukon"><img src="{yukon}" alt="Yukon Trail" /></a>
        </div>
        <div class="card-content">
          <div class="location">Canada</div>
          <h2><a href="/projets/yukon">Yukon Arctic Ultra</a></h2>
          <h3>La course la plus froide du monde</h3>
          <p>
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ad aliquid amet aspernatur dolorum eligendi esse
            fugiat ipsa ipsam labore laudantium magnam magni molestiae nemo nobis placeat quae quibusdam sint, veniam.
          </p>
          <a href="/projets/yukon" class="more">
            Lire la suite
            <span class="icon"><Icon icon="material-symbols:arrow-forward-ios" /></span>
          </a>
        </div>
      </div>

      <div class="card">
        <div class="card-image">
          <a href="/projets/grand-to-grand"><img src="{grandToGrand}" alt="Grand to Grand"></a>
        </div>
        <div class="card-content">
          <div class="location">Arizona USA</div>
          <h2><a href="/projets/grand-to-grand">Grand to Grand</a></h2>
          <h3>Un ultra-trail de 270 km en Utah</h3>
          <p>
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Accusantium alias aliquam assumenda dolorem, eos
            error eum in maxime molestiae officia placeat porro quaerat quam, quibusdam quidem saepe vel vero. Sapiente!
          </p>
          <a href="/projets/grand-to-grand" class="more">
            Lire la suite
            <span class="icon"><Icon icon="material-symbols:arrow-forward-ios" /></span>
          </a>
        </div>
      </div>

      <div class="card">
        <div class="card-image">
          <a href="/projets/mds"><img src="{mds}" alt="Marathon des sables"></a>
        </div>
        <div class="card-content">
          <div class="location">Maroc</div>
          <h2><a href="/projets/mds">Marathon des sables</a></h2>
          <h3>Au coeur du Sahara Marocain</h3>
          <p>
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Accusantium alias aliquam assumenda dolorem, eos
            error eum in maxime molestiae officia placeat porro quaerat quam, quibusdam quidem saepe vel vero. Sapiente!
          </p>
          <a href="/projets/mds" class="more">
            Lire la suite
            <span class="icon"><Icon icon="material-symbols:arrow-forward-ios" /></span>
          </a>
        </div>
      </div>
    </div>

    <p class="has-text-centered">
      <a href="/association" class="button">
        Soutenir l'association
        <span class="icon"><Icon icon="material-symbols:arrow-forward-ios" /></span>
      </a>
    </p>
  </div>
</div>

<style lang="sass">
  @use '$lib/sass/utilities/variables' as *
  @use '$lib/sass/utilities/mixins' as *

  .wrapper
    background-color: #fff
    background-image: url("../../../lib/images/bg-green-dots.jpg")
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
      h2
        font-family: 'Anton', sans-serif
        text-transform: uppercase
        font-size: 40px
        line-height: 50px
        margin: 0

        a
          color: $secondary
          text-decoration: none
          transition: color 200ms ease

          &:hover
            color: $secondary-dark

      h3
        font-size: 22px
        margin: 0

      p
        line-height: 24px
        margin: 1rem 0

      a
        &.more
          color: $secondary
          text-decoration: none
          transition: all 200ms ease

          &:hover
            color: $secondary-dark
            text-decoration: underline

          .icon
            font-size: 12px
</style>