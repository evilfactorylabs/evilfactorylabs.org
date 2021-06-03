<script>
  import { fade } from 'svelte/transition'

  import Hero from '../components/Hero'
  import Typewriter from '../components/Typewriter'
  import Transition from '../components/Transition'
  import Container from '../components/Container'
</script>

<style>
  .o-video {
    position: absolute;
    min-width: 100%;
    min-height: 100%;
    max-width: 100%;
    object-fit: cover;
    left: 0;
    top: 0;
  }

  .o-backdrop {
    position: fixed;
    left: 0;
    bottom: 0;
    background: rgba(0, 0, 0, 0.8);
    width: 100%;
  }

  .o-footer {
    position: fixed;
    bottom: 0;
    right: 0;
    width: 100%;
    font-weight: bold;
    text-align: center;
    text-transform: uppercase;
    padding: 2rem;
    padding-bottom: 3rem;
  }

  @media screen and (min-width: 60em) {
    .o-footer {
      text-align: right;
      padding-right: 5rem;
    }
  }
</style>

<svelte:head>
  <title>evilfactorylabs.org - Beranda</title>
</svelte:head>

<Transition>
  <video autoplay muted loop class="o-video">
    <source src="/bg.mp4" type="video/mp4" />
  </video>

  <div class="o-backdrop">
    <Container>
      <Hero>
        <Typewriter cursor={false} interval={65}>
          <h2 class="o-cta__title o-cta__title--is-primary u-mb-sm">
            We have principles in empowering community. You in?
          </h2>
        </Typewriter>
        <a
          class="o-cta__action"
          href="/kiprah"
          in:fade={{ duration: 666, delay: 3800 }}>
          If you wanna know how, click here.
        </a>
      </Hero>
    </Container>

    <div class="o-footer">
      <a class="u-td-none" href="https://evlfctry.pro/contact">
        evlfctry.pro/contact
      </a>
    </div>
  </div>
</Transition>
