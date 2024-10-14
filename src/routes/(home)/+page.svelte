<script>
  import Announcement from './Announcement.svelte';
  import Hero from './Hero.svelte';
  import Projects from './Projects.svelte';
  import Donate from '../Donate.svelte';
</script>

<svelte:head>
  <title>OUT'CHA - Sport for All</title>
  <meta name="description"
        content="Association qui a pour but de favoriser l'inclusion sociale et la réalisation de rêves par le sport." />
</svelte:head>

<Hero />
{#if new Date() <= new Date('2024-11-10')}
  <Announcement />
{/if}
<Projects />
<Donate />