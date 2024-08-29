<script>
  import { onMount } from "svelte";
  import Icon from '@iconify/svelte';
  import aventuresPolaires from '$lib/images/Aventures-Polaires-2024.jpeg';

  let active = false;

  onMount(() => {
    active = true;
  })
</script>

<div class="modal {active ? 'is-active' : ''}">
  <div class="modal-background" on:click={() => active = false}></div>
  <div class="modal-card">
    <header class="modal-card-head px-4 py-3">
      <h2 class="subtitle has-text-weight-semibold">Gardiens de cabane</h2>
    </header>
    <section class="modal-card-body has-text-centered p-3">
      <iframe width="100%" height="315" src="https://www.youtube.com/embed/nGiP-QMJmGY?si=TgLCFJ7RSu-bldPk" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
    </section>
    <footer class="modal-card-foot px-4 py-3">
      <p>Rendez-vous du 14 au 21 Septembre 2024 à la cabane du Plan Névé !!!</p>
    </footer>
  </div>
  <button class="modal-close is-large" aria-label="close" on:click={() => active = false}></button>
</div>

<div class="container mt-3">
  <div class="notification is-warning is-light is-clearfix">
    <span class="icon">
      <Icon icon="fa6-solid:bullhorn" />
    </span>
    <strong>Gardiens de cabane :</strong>
    Retrouvez-nous du 14 au 21 Septembre à la cabane du Plan Névé !!!
    (<a href="#" on:click|preventDefault={() => active = true}>En savoir plus</a>)
  </div>
</div>
