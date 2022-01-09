<script>
  import { fade } from 'svelte/transition'

  import Hero from '../components/Hero'
  import Container from '../components/Container'
  import Transition from '../components/Transition'
</script>

<svelte:head>
  <title>evilfactorylabs.org - Kiprah</title>
</svelte:head>

<Transition>
  <Container>
    <h2 class="o-cta__title u-mb-sm" in:fade={{ duration: 1000, delay: 500 }}>
      Take a part
    </h2>
    <div in:fade={{ duration: 1000, delay: 1000 }}>
      <Hero>
        <p class="u-fs-md u-fs-sm--xs u-mb-sm">
          Our main focus is to educate. Learning by
          <strike>teaching</strike>
          sharing is such a bullshit but unfortunately it works.
        </p>
        <p class="u-fs-md u-fs-sm--xs u-mb-sm">
          We frequently sharing what we learned by writing on this
          <a href="//evilfactorylabs.org">small blog,</a>
          if you are interested to do so, yes, just ping us.
        </p>
        <p class="u-fs-md u-fs-sm--xs u-mb-sm">
          Feeling adventurous? We are having fun with some bleeding-edge
          technologies (and we have some secret projects that only 33° knows).
          The good news was our projects are Open Source and always will be.
          Here is our
          <a href="https://github.com/evilfactorylabs">GitHub,</a>
          you know what you should do.
        </p>
        <p class="u-fs-md u-fs-sm--xs u-mb-sm">
          But if you don't, just ping us.
        </p>
      </Hero>
    </div>
  </Container>
</Transition>
