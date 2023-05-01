<script>
  import Project from '../Project.svelte';
  import Gallery from '../Gallery.svelte';

  import photo1 from '$lib/images/projets/yukon/photo1.webp';
  import photo2 from '$lib/images/projets/yukon/photo2.webp';
  import photo3 from '$lib/images/projets/yukon/photo3.webp';
  import photo4 from '$lib/images/projets/yukon/photo4.webp';
  import photo5 from '$lib/images/projets/yukon/photo5.webp';
  import photo6 from '$lib/images/projets/yukon/photo6.webp';
  import photo7 from '$lib/images/projets/yukon/photo7.webp';
  import photo8 from '$lib/images/projets/yukon/photo8.webp';
  import photo9 from '$lib/images/projets/yukon/photo9.webp';
  import photo10 from '$lib/images/projets/yukon/photo10.webp';

  const images = [
    { image: photo1, width: 1024, height: 768 },
    { image: photo2, width: 715, height: 800 },
    { image: photo3, width: 768, height: 1024 },
    { image: photo4, width: 1067, height: 800 },
    { image: photo5, width: 1067, height: 800 },
    { image: photo6, width: 1027, height: 800 },
    { image: photo7, width: 1007, height: 800 },
    { image: photo8, width: 960, height: 1280 },
    { image: photo9, width: 960, height: 984 },
    { image: photo10, width: 960, height: 720 },
  ]
</script>

<svelte:head>
  <title>OUT'CHA - North Cape</title>
</svelte:head>

<Project name="Yukon Arctic Ultra">
  <div slot="content">
    <h3 class="m-0">Canada</h3>
    <h1>Yukon Arctic Ultra</h1>
    <h2>La course la plus froide du monde</h2>

    <section class="mb-4">
      <p>
        Lorem ipsum dolor sit amet, consectetur adipisicing elit. Adipisci animi autem consequuntur cum, cupiditate
        delectus eius ex facere facilis fugit necessitatibus nesciunt quam, quos sapiente tempora tempore ullam. Minima,
        quasi!
      </p>

      <p>
        <iframe width="100%" height="340" src="https://www.youtube.com/embed/yLOG3ipbeNg"
                title="YouTube video player"
                frameborder="0"
                allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
                allowfullscreen></iframe>
      </p>
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

      <p><img src={photo10} alt="Yukon Arctic Ultra" class="is-pulled-left mr-4 my-1" width="250" /></p>

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
      <p><img src={photo3} alt="Yukon Arctic Ultra" class="is-pulled-right ml-4 my-1" width="200" /></p>
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
