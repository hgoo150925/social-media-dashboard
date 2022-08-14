<script>
  import Switch from './Switch.svelte';
</script>

<main>
  <header class="header">
    <div class="container__header ">
      <h1>Social Media Dashboard</h1>
      <h3>Total Followers: 23,004</h3>
    </div>
    <div class="toggle">
      <span> Dark Mode</span>
      <Switch />
    </div>
  </header>
</main>

<style>
  .header {
    display: flex;
    justify-content: space-between;
  }
  .container__header h1 {
    color: #fff;
    font-size: 3.5rem;
  }
  .container__header h3 {
    color: var(--Desaturated-Blue-Text);
    font-size: 1.5rem;
  }
  .container__header {
    line-height: 1.5;
  }
  .toggle span {
    color: var(--Desaturated-Blue-Text);
    font-size: 1.5rem;
  }
  .toggle {
    display: flex;
    align-items: center;
    justify-content: center;
  }

  :global(body.dark-mode) .container__header h1 {
    color: var(--Very-Dark-Blue-TopBGPattern);
  }

  :global(body.dark-mode) .toggle span {
    color: var(--Desaturated-Blue-Text);
  }
</style>
