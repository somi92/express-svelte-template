<script>
  import { onMount } from 'svelte';

  export let name;

  let data = '';

  onMount(async function() {
    const response = await fetch('http://localhost:8080/hello');
    data = (await response.json()).data;
  });
</script>

<style>
  main {
    text-align: center;
    padding: 1em;
    max-width: 240px;
    margin: 0 auto;
  }

  h1 {
    color: #ff3e00;
    text-transform: uppercase;
    font-size: 4em;
    font-weight: 100;
  }

  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }

  .loader {
    border: 2px solid #f3f3f3;
    border-top: 2px solid #ff3e00;
    border-radius: 50%;
    width: 20px;
    height: 20px;
    animation: spin 2s linear infinite;
    margin: auto;
  }

  @keyframes spin {
    0% {
      transform: rotate(0deg);
    }
    100% {
      transform: rotate(360deg);
    }
  }
</style>

<main>
  <h1>Hello {name}!</h1>
  <p>
    Access the docs on
    <a href="https://svelte.dev/tutorial">Express</a>
    to learn how to build Node.js web apps.
  </p>
  <p>
    Visit the
    <a href="https://svelte.dev/tutorial">Svelte tutorial</a>
    to learn how to build Svelte apps.
  </p>
  <br />
  {#if data}
    <p>
      <i>{data}</i>
    </p>
  {:else}
    <div class="loader" />
  {/if}
</main>
