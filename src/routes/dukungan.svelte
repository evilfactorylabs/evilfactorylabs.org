<script>
  import { fade } from 'svelte/transition'

  import Hero from '../components/Hero'
  import Container from '../components/Container'
  import Transition from '../components/Transition'
</script>

<svelte:head>
  <title>evilfactorylabs.org - Dukung(an)</title>
</svelte:head>

<Transition>
  <Container>
    <h2 class="o-cta__title u-mb-sm" in:fade={{ duration: 1000, delay: 500 }}>
      Help us to help you.
    </h2>
    <div in:fade={{ duration: 1000, delay: 1000 }}>
      <Hero>
        <p class="u-fs-md u-fs-sm--xs u-mb-sm">
          Currently we have
          <a href="https://perkumpulan.evilfactory.id">public forum.</a>
          Beside that, we do
          <a href="https://twitter.com/evilfactorylabs">tweeting</a>
          very often. Just ping us, we are very friendly, seriously.
        </p>
        <p class="u-fs-md u-fs-sm--xs u-mb-sm">
          Yes, you can ask anything: Programming, Life, Blogging, you name it.
        </p>
        <p class="u-fs-md u-fs-sm--xs u-mb-sm">
          If you love with what we did & want to support us,
          <a href="https://trakteer.id/evilfactorylabs">go to here.</a>
          Thanks!
        </p>
      </Hero>
    </div>
  </Container>
</Transition>
