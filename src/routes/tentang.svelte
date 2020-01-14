<script>
  import { fade } from 'svelte/transition'

  import Hero from '../components/Hero'
  import Container from '../components/Container'
  import Transition from '../components/Transition'
</script>

<svelte:head>
  <title>evilfactorylabs.org - Tentang</title>
</svelte:head>

<Transition>
  <Container>
    <h2 class="o-cta__title u-mb-sm" in:fade={{ duration: 1000, delay: 500 }}>
      We are a
      <strike>company</strike>
      community
    </h2>
    <div in:fade={{ duration: 1000, delay: 1000 }}>
      <Hero>
        <p class="u-fs-md u-fs-sm--xs u-mb-md">
          evilfactorylabs exists to trying bridging the
          <em>skills gap</em>
          in IT industry in Indonesia.
        </p>
        <a class="o-cta__action" href="/cerita">Wanna know the long story?</a>
      </Hero>
    </div>
  </Container>
</Transition>
