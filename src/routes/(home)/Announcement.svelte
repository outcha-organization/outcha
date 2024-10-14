<script>
  import { onMount } from "svelte";
  import Icon from '@iconify/svelte';
  import surLeFil from '$lib/images/SUR-LE-FIL-Montbenon.jpeg';

  let active = false;

  onMount(() => {
    active = true;
  })
</script>

<div class="modal {active ? 'is-active' : ''}">
  <div class="modal-background" on:click={() => active = false}></div>
  <div class="modal-content">
    <p class="image is-3by4">
      <a href="https://monbillet.ch/events/sur-le-fil-24-aventures-humaines-sportives" target="_blank" rel="noreferrer">
        <img src="{surLeFil}" alt="SUR LE FIL Lutry - Cap Nord" />
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
    <strong>SUR LE FIL :</strong>
    Le film d'aventure avec Patrick Sumi à Lausanne le 9 Novembre 2024 !!!
    (<a href="#" on:click|preventDefault={() => active = true}>En savoir plus</a>)
  </div>
</div>
