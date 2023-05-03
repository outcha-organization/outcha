<script>
  import Project from '../Project.svelte';
  import Gallery from '../Gallery.svelte';

  import cover from '$lib/images/projets/grand-to-grand/cover.webp';
  import photo1 from '$lib/images/projets/grand-to-grand/photo1.webp';
  import photo2 from '$lib/images/projets/grand-to-grand/photo2.webp';
  import photo3 from '$lib/images/projets/grand-to-grand/photo3.webp';
  import photo4 from '$lib/images/projets/grand-to-grand/photo4.webp';
  import photo5 from '$lib/images/projets/grand-to-grand/photo5.webp';
  import photo6 from '$lib/images/projets/grand-to-grand/photo6.webp';

  const images = [
    { image: photo1, width: 768, height: 1024 },
    { image: photo2, width: 1024, height: 768 },
    { image: photo3, width: 1024, height: 768 },
    { image: photo4, width: 1024, height: 768 },
    { image: photo5, width: 768, height: 1024 },
    { image: photo6, width: 1024, height: 768 }
  ]
</script>

<svelte:head>
  <title>OUT'CHA - North Cape</title>
</svelte:head>

<Project name="Grand to Grand">
  <div slot="content">
    <h3 class="m-0">Aventure / Arizona USA</h3>
    <h1>Grand to Grand</h1>
    <h2>Un ultra-trail de 270 km en Utah</h2>

    <section class="mb-4">
      <p>
        Lorem ipsum dolor sit amet, consectetur adipisicing elit. Adipisci animi autem consequuntur cum, cupiditate
        delectus eius ex facere facilis fugit necessitatibus nesciunt quam, quos sapiente tempora tempore ullam. Minima,
        quasi!
      </p>

      <p><img src={cover} alt="Grand to Grand" /></p>
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

      <p><img src={photo1} alt="Grand to Grand" class="is-pulled-left mr-4 my-1" width="200" /></p>

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
      <p><img src={photo2} alt="Grand to Grand" class="is-pulled-right ml-4 my-1" width="250" /></p>
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
