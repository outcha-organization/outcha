<script>
  import { onMount } from 'svelte';
  import Icon from '@iconify/svelte';
  import Swiper, { Navigation } from 'swiper';
  import 'swiper/css';

  import freudeHerrscht from '$lib/images/home/partners/freude-herrscht.png';
  import baechli from '$lib/images/home/partners/baechli.png';
  import maiday from '$lib/images/home/partners/maiday.png';
  import compex from '$lib/images/home/partners/compex.png';
  import bgcm from '$lib/images/home/partners/bgcm.png';
  import bonvin from '$lib/images/home/partners/bonvin.png';
  import bcv from '$lib/images/home/partners/bcv.png';
  import michot from '$lib/images/home/partners/michot.png';

  onMount(() => {
    new Swiper('.swiper', {
      modules: [Navigation],
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

<section class="wrapper">
  <div class="container">
    <div class="swiper-button-prev">
      <Icon icon="material-symbols:arrow-back-ios-new" />
    </div>
    <div class="swiper">
      <div class="swiper-wrapper">
        <a class="swiper-slide" href="https://www.freude-herrscht.ch/fran%C3%A7ais/" target="_blank">
          <img src="{freudeHerrscht}" alt="Freude herrscht" />
        </a>
        <a class="swiper-slide" href="https://www.baechli-bergsport.ch/fr" target="_blank">
          <img src="{baechli}" alt="Bächli" />
        </a>
        <a class="swiper-slide" href="https://maiday.ch/" target="_blank">
          <img src="{maiday}" alt="Maiday" />
        </a>
        <a class="swiper-slide" href="https://www.compex.com/ch/fr/" target="_blank">
          <img src="{compex}" alt="Compex" />
        </a>
        <a class="swiper-slide" href="https://bgcm.ch/" target="_blank">
          <img src="{bgcm}" alt="BGCM" />
        </a>
        <a class="swiper-slide" href="https://bonvin1858.ch/" target="_blank">
          <img src="{bonvin}" alt="Bonvin" />
        </a>
        <a class="swiper-slide" href="https://www.bcv.ch/" target="_blank">
          <img src="{bcv}" alt="BCV" />
        </a>
        <a class="swiper-slide" href="http://eventente.ch/" target="_blank">
          <img src="{michot}" alt="Michot Eventente" />
        </a>
      </div>
    </div>
    <div class="swiper-button-next">
      <Icon icon="material-symbols:arrow-forward-ios" />
    </div>
  </div>
</section>

<style lang="sass">
  @use '$lib/sass/utilities/variables' as *
  @use '$lib/sass/utilities/mixins' as *

  .container
    display: flex
    gap: 10px
    margin-top: 10px

  .swiper-wrapper
    flex-grow: 1

  .swiper-button-prev,
  .swiper-button-next
    display: flex
    justify-content: center
    align-items: center
    cursor: pointer
    color: $grey
    font-size: 32px
    transition: color 200ms ease

    &:hover
      color: $grey-dark
</style>
