<script>
  import svelteLogo from './assets/svelte.svg'
  import viteLogo from '/vite.svg'
  import Counter from './lib/Counter.svelte'
  import Card from './lib/Card.svelte';
  import TaxToggle from './lib/TaxToggle.svelte';

  const data = [{
    title: "Product 1",
    description: "This is a product you can buy only here",
    price: 23.30,
  },
  {
    title: "Product 2",
    description: "This is a product you can buy only here",
    price: 60,
  },
  {
    title: "Product 3",
    description: "This is a product you can buy only here",
    price: 10.15,
  }]
</script>

<main>
  <div>
    <a href="https://vite.dev" target="_blank" rel="noreferrer">
      <img src={viteLogo} class="logo" alt="Vite Logo" />
    </a>
    <a href="https://svelte.dev" target="_blank" rel="noreferrer">
      <img src={svelteLogo} class="logo svelte" alt="Svelte Logo" />
    </a>
  </div>
  <h1>Vite + Svelte</h1>

  <div class="card">
    <Counter />
  </div>

  <div class="card">
    <TaxToggle />
  </div>

  <div class="card">
    {#each data as item}
		  <Card {...item} />
	  {/each}
  </div>

  <p>
    Check out <a href="https://github.com/sveltejs/kit#readme" target="_blank" rel="noreferrer">SvelteKit</a>, the official Svelte app framework powered by Vite!
  </p>

  <p class="read-the-docs">
    Click on the Vite and Svelte logos to learn more
  </p>
</main>

<style>
  :global(.button) {
    background-color: grey;
    color: black;
    border-width: 5px;
  }

  .logo {
    height: 6em;
    padding: 1.5em;
    will-change: filter;
    transition: filter 300ms;
  }
  .logo:hover {
    filter: drop-shadow(0 0 2em #646cffaa);
  }
  .logo.svelte:hover {
    filter: drop-shadow(0 0 2em #ff3e00aa);
  }
  .read-the-docs {
    color: #888;
  }
</style>
