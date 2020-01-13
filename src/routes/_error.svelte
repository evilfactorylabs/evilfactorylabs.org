<script>
  import Container from '../components/Container'

  export let status
  export let error

  const dev = process.env.NODE_ENV === 'development'
</script>

<style>
  h1,
  p {
    margin: 0 auto;
  }

  h1 {
    font-size: 2.8em;
    font-weight: 700;
    margin: 0 0 0.5em 0;
  }

  p {
    font-size: 2rem;
    margin: 1em auto;
  }

  @media (min-width: 480px) {
    h1 {
      font-size: 4em;
    }
  }
</style>

<svelte:head>
  <title>{status} - {error.message}</title>
</svelte:head>

<Container>
  <h1>{status}</h1>

  <p>{error.message}. But we have trace this, thank you.</p>

  <a href="/">Back to home</a>

  {#if dev && error.stack}
    <pre>{error.stack}</pre>
  {/if}
</Container>
