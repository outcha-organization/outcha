<script>
  import { onMount } from 'svelte';
  import Swiper from 'swiper';
  import 'swiper/css';
  import Banner from "../Banner.svelte";
  import banner from '$lib/images/association/banner.webp';
  import Icon from '@iconify/svelte';

  import grandToGrand1 from '$lib/images/association/projects/grand-to-grand-1.webp';
  import grandToGrand2 from '$lib/images/association/projects/grand-to-grand-2.webp';
  import grandToGrand3 from '$lib/images/association/projects/grand-to-grand-3.webp';
  import lapland1 from '$lib/images/association/projects/lapland-1.webp';
  import lapland2 from '$lib/images/association/projects/lapland-2.webp';
  import lapland3 from '$lib/images/association/projects/lapland-3.webp';
  import mds1 from '$lib/images/association/projects/mds-1.webp';
  import mds2 from '$lib/images/association/projects/mds-2.webp';
  import mds3 from '$lib/images/association/projects/mds-3.webp';
  import yukon1 from '$lib/images/association/projects/yukon-1.webp';
  import yukon2 from '$lib/images/association/projects/yukon-2.webp';
  import yukon3 from '$lib/images/association/projects/yukon-3.webp';

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
          <a href="/projets/grand-to-grand" class="swiper-slide"><img src={grandToGrand2} /></a>
          <a href="/projets/mds" class="swiper-slide"><img src={mds3} /></a>
          <a href="/projets/laponie" class="swiper-slide"><img src={lapland2} /></a>
          <a href="/projets/grand-to-grand" class="swiper-slide"><img src={grandToGrand1} /></a>
          <a href="/projets/laponie" class="swiper-slide"><img src={lapland3} /></a>
          <a href="/projets/grand-to-grand" class="swiper-slide"><img src={grandToGrand3} /></a>
          <a href="/projets/mds" class="swiper-slide"><img src={mds2} /></a>
          <a href="/projets/laponie" class="swiper-slide"><img src={lapland1} /></a>
          <a href="/projets/mds" class="swiper-slide"><img src={mds1} /></a>
          <a href="/projets/yukon" class="swiper-slide"><img src={yukon3} /></a>
          <a href="/projets/yukon" class="swiper-slide"><img src={yukon2} /></a>
          <a href="/projets/yukon" class="swiper-slide"><img src={yukon1} /></a>
        </div>
        <div class="swiper-pagination"></div>
      </div>

      <p>
        <a href="/projets" class="button">
          Voir tous les projets
          <span class="icon"><Icon icon="material-symbols:arrow-forward-ios" /></span>
        </a>
      </p>

      <h2>Aidez nous</h2>
      <div class="card">
        <h3>Pour soutenir le projet:</h3>
        IBAN: CH53 0076 7000 S546 2495 4<br>
        Numéro TWINT : 078 958 06 26
      </div>
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

    .card
      text-align: center
      line-height: 24px
</style>