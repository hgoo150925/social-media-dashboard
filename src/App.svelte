<script lang="ts">
  import Social from './lib/Social.svelte';
</script>

<main>
  <div class="container">
    <Social />
  </div>
</main>

<style>
  .container {
    margin: 3rem auto;
    max-width: 144rem;
  }
  :global(body.dark-mode) {
    background-color: var(--White-BG);
    color: #bfc2c7;
  }
</style>
