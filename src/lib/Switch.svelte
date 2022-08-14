<script lang="ts">
  let darkMode = false;
  const toggle = (): void => {
    darkMode = !darkMode;
    window.document.body.classList.toggle('dark-mode');
  };
</script>

<main>
  <button class="switch" on:click={toggle}>
    {#if darkMode}
      Ok
    {:else}
      Oki
    {/if}
  </button>
</main>

<style>
  .switch {
    width: 10rem;
    background: violet;
  }
</style>
