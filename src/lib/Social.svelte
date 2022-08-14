<script>
  import Header from './Header.svelte';

  import { data } from '../data';
</script>

<main>
  <Header />
  <div class="grid-container">
    {#each data as { image, user, followers, text, up, today }}
      <article class="grid-item ">
        <div class="user">
          <img src={image} alt="social-media" />
          <h1>{user}</h1>
        </div>
        <div class="text">
          <p>{followers}</p>
          <p>{text}</p>
        </div>
        <p>{up} {today}</p>
      </article>
    {/each}
  </div>
</main>

<style>
  .grid-container {
    color: #fff;
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    grid-template-rows: 1fr;
    gap: 1rem;
    margin: 4.2rem 0 0 0;
    overflow: hidden;
  }
  .grid-item {
    background-color: var(--Dark-Desaturated-Blue-CardBG);
    border-radius: 0.5rem;

    height: 22.6rem;
  }
  .user {
    display: flex;

    gap: 1rem;
    margin: 0 0 0 0.5rem;
  }
  .text {
    padding: 0.5rem;
    margin: 0 auto;
  }
  .text p:nth-child(1) {
    font-size: 5.6rem;
    color: #fff;
  }
  :global(body.dark-mode) .grid-item {
    background-color: var(--Light-Grayish-Blue-CardBG);
  }

  :global(body.dark-mode) .grid-item h1 {
    color: var(--Desaturated-Blue-Text);
  }

  :global(body.dark-mode) .grid-item p {
    color: #000;
  }
</style>
