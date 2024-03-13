<script>
  import { onMount } from "svelte";
  import Icon from '@iconify/svelte';
  import aventuresPolaires from '$lib/images/Aventures-Polaires-2024.jpeg';

  let active = false;

  onMount(() => {
    // active = true;
  })
</script>

<div class="modal {active ? 'is-active' : ''}">
  <div class="modal-background" on:click={() => active = false}></div>
  <div class="modal-content">
    <p class="image is-3by4">
      <a href="https://reservation.anzere.ch/05-04-2024-aventures-polaires.html" target="_blank" rel="noreferrer">
        <img src="{aventuresPolaires}" alt="Aventures Polaires" />
      </a>
    </p>
  </div>
  <button class="modal-close is-large" aria-label="close" on:click={() => active = false}></button>
</div>

<div class="container mt-3">
  <div class="notification is-warning is-light is-clearfix">
    <span class="icon">
      <Icon icon="fa6-solid:bullhorn" />
    </span>
    <strong>Aventures Polaires :</strong>
    Rendez-vous le 5 Avril 2024 18:30 à Anzère !!!
    (<a href="#" on:click|preventDefault={() => active = true}>En savoir plus</a>)
  </div>
</div>
