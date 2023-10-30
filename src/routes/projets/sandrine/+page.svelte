<script>
  import Project from '../Project.svelte';
  import Gallery from '../Gallery.svelte';

  import photo1 from '$lib/images/projets/sandrine/photo1.webp';
  import photo2 from '$lib/images/projets/sandrine/photo2.webp';
  import photo3 from '$lib/images/projets/sandrine/photo3.webp';
  import photo4 from '$lib/images/projets/sandrine/photo4.webp';
  import photo5 from '$lib/images/projets/sandrine/photo5.webp';
  import photo6 from '$lib/images/projets/sandrine/photo6.webp';
  import photo7 from '$lib/images/projets/sandrine/photo7.webp';
  import photo8 from '$lib/images/projets/sandrine/photo8.webp';
  import photo9 from '$lib/images/projets/sandrine/photo9.webp';
  import photo10 from '$lib/images/projets/sandrine/photo10.webp';
  import photo11 from '$lib/images/projets/sandrine/photo11.webp';
  import photo12 from '$lib/images/projets/sandrine/photo12.webp';

  const images = [
    { image: photo1, width: 1600, height: 1200 },
    { image: photo2, width: 1200, height: 1600 },
    { image: photo3, width: 1600, height: 720 },
    { image: photo4, width: 1200, height: 1600 },
    { image: photo5, width: 1200, height: 1600 },
    { image: photo6, width: 1200, height: 1600 },
    { image: photo7, width: 1600, height: 1200 },
    { image: photo8, width: 1600, height: 1200 },
    { image: photo9, width: 1600, height: 1200 },
    { image: photo10, width: 1600, height: 1200 },
    { image: photo11, width: 1600, height: 1200 },
    { image: photo12, width: 1600, height: 1200 }
  ]
</script>

<svelte:head>
  <title>OUT'CHA - North Cape</title>
</svelte:head>

<Project name="Sandrine">
  <div slot="content">
    <h3 class="m-0">Suisse</h3>
    <h1>Sandrine</h1>
    <h2>Courir Sierre-Zinal en étant aveugle</h2>

    <section class="mb-4">
      <p>
        Lorem ipsum dolor sit amet, consectetur adipisicing elit. Adipisci animi autem consequuntur cum, cupiditate
        delectus eius ex facere facilis fugit necessitatibus nesciunt quam, quos sapiente tempora tempore ullam. Minima,
        quasi!
      </p>

      <p><img src={photo3} alt="Sandrine" /></p>
    </section>

    <section class="is-clearfix mb-4">
      <p>
        Lorem ipsum dolor sit amet, consectetur adipisicing elit. At debitis dolorem, enim impedit modi nam officia quam
        quisquam tempora temporibus. Ab accusamus corporis distinctio eveniet impedit libero maiores nam rerum.
      </p>

      <h3>Lorem Ipsum</h3>
      <p>
        Lorem ipsum dolor sit amet, consectetur adipisicing elit. Debitis deleniti dolorum exercitationem molestiae odio
        quisquam reprehenderit! A ad debitis eaque fugit harum illo laborum modi molestias officia praesentium,
        repudiandae suscipit?
      </p>

      <p><img src={photo8} alt="Sandrine" class="is-pulled-left mr-4 my-1" width="250" /></p>

      <p>
        Lorem ipsum dolor sit amet, consectetur adipisicing elit. Alias architecto at corporis, cum delectus deleniti
        dolor dolores ea eos expedita, explicabo facere magnam magni provident quia ratione rerum saepe
        voluptatibus?
      </p>

      <h4>Dolor sit amet</h4>
      <p>
        Lorem ipsum dolor sit amet, consectetur adipisicing elit. Alias architecto at corporis, cum delectus deleniti
        dolor dolores ea eos expedita, explicabo facere magnam magni provident quia ratione rerum saepe
        voluptatibus?
      </p>
    </section>

    <section class="is-clearfix mb-4">
      <h3>Alias architecto at corporis</h3>
      <p><img src={photo2} alt="Sandrine" class="is-pulled-right ml-4 my-1" width="200" /></p>
      <p>
        Lorem ipsum dolor sit amet, consectetur adipisicing elit. Alias architecto at corporis, cum delectus deleniti
        dolor dolores ea eos expedita, explicabo facere magnam magni provident quia ratione rerum saepe
        voluptatibus?
      </p>
      <p>
        Lorem ipsum dolor sit amet, consectetur adipisicing elit. Alias architecto at corporis, cum delectus deleniti
        dolor dolores ea eos expedita, explicabo facere magnam magni provident quia ratione rerum saepe
        voluptatibus?
      </p>
    </section>
  </div>

  <div slot="sidebar">
    <Gallery images={images} />
  </div>
</Project>
