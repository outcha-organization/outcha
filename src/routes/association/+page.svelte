<script>
  import { onMount } from 'svelte';
  import Swiper from 'swiper';
  import 'swiper/css';
  import Banner from "../Banner.svelte";
  import banner from '$lib/images/association/banner.webp';
  import Icon from '@iconify/svelte';
  import Donate from '../Donate.svelte';

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
    new Swiper('.swiper', {
      slidesPerView: 3,
      spaceBetween: 20,
      loop: true,
      autoplay: {
        delay: 2500,
        disableOnInteraction: false,
      },
      navigation: {
        prevEl: '.swiper-button-prev',
        nextEl: '.swiper-button-next'
      },
      breakpoints: {
        768: {
          slidesPerView: 5,
          spaceBetween: 35,
        },
        1024: {
          slidesPerView: 6,
          spaceBetween: 20,
        }
      }
    });
  })
</script>

<svelte:head>
  <title>OUT'CHA - L'association</title>
  <meta name="description"
        content="Association qui a pour but de favoriser l'inclusion sociale et la réalisation de rêves par le sport." />
</svelte:head>

<Banner title="L'association" image={banner} />

<div class="wrapper">
  <section class="about">
    <div class="container">
      <h1><em>Outdoor</em> Challenges</h1>
      <p>
        L’association a pour but de favoriser l’inclusion sociale,
        l’épanouissement, la réalisation de rêves et le partage par le sport,
        d’encourager la pratique du sport dans le respect de la nature,
        de promouvoir les échanges socio-culturels et l’intégration
        des valeurs sportives, chez les jeunes à travers le sport et les défis.
      </p>

      <div class="swiper mySwiper">
        <div class="swiper-wrapper">
          <a href="/projets#camps" class="swiper-slide"><img src={freudeHerrscht2} /></a>
          <a href="/projets#montagne" class="swiper-slide"><img src={afghansMontagne2} /></a>
          <a href="/projets#montagne" class="swiper-slide"><img src={afghansMontagne} /></a>
          <a href="/projets#camps" class="swiper-slide"><img src={freudeHerrscht} /></a>
          <a href="/projets#camps" class="swiper-slide"><img src={freudeHerrscht3} /></a>
          <a href="/projets#montagne" class="swiper-slide"><img src={afghansMontagne3} /></a>
          <a href="/projets#sandrine" class="swiper-slide"><img src={sandrine3} /></a>
          <a href="/projets#sandrine" class="swiper-slide"><img src={sandrine2} /></a>
          <a href="/projets#sandrine" class="swiper-slide"><img src={sandrine} /></a>
          <a href="/projets#ski" class="swiper-slide"><img src={afghansSki3} /></a>
          <a href="/projets#ski" class="swiper-slide"><img src={afghansSki2} /></a>
          <a href="/projets#ski" class="swiper-slide"><img src={afghansSki} /></a>
        </div>
        <div class="swiper-pagination"></div>
      </div>

      <p>
        <a href="/projets" class="button">
          Voir tous les projets
          <span class="icon"><Icon icon="material-symbols:arrow-forward-ios" /></span>
        </a>
      </p>

      <Donate />
    </div>
  </section>
</div>

<style lang="sass">
  .wrapper
    background-color: #fff
    background-image: url("../../../lib/images/bg-green-dots.jpg")
    background-size: cover
    padding: 30px 0
    min-height: 350px

  h1
    font-family: 'Anton', sans-serif
    font-weight: 400
    font-size: 55px
    text-transform: uppercase
    line-height: 1
    margin: 0 0 24px 0
    text-align: center

    em
      font-family: 'Great Sejagad', sans-serif
      color: $primary
      display: block
      font-size: 45px
      font-weight: 400
      line-height: .9
      position: relative

  h2
    font-family: 'Anton', sans-serif
    font-weight: 400
    font-size: 24px
    text-transform: uppercase
    line-height: 1
    margin: 0
    text-align: center

  h3
    margin: 12px 0
    font-size: 18px
    font-weight: 700

  .about
    padding-bottom: 30px

    p
      margin: 40px 0
      font-size: 18px
      font-weight: 500
      line-height: 30px
      text-align: center
</style>