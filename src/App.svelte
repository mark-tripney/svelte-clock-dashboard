<script>
  import Clock from './components/Clock.svelte';
  import Button from './components/Button.svelte';
  const handleButtonClick = () => console.log('Click');
</script>

<main>
  <Clock />
  <Button on:click={handleButtonClick} />
</main>
