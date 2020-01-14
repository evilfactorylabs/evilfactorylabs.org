<script>
  import { fade } from 'svelte/transition'

  import Container from '../components/Container'
  import Transition from '../components/Transition'
  import Hero from '../components/Hero'
</script>

<style>
  ._some-block {
    display: inline-block;
    margin-right: 3rem;
    margin-top: 1rem;
    margin-bottom: 2rem;
    text-align: center;
  }

  ._some-block > i {
    color: var(--primary-color);
    display: inline-block;
    font-size: 1.8rem;
    line-height: 0;
    padding-right: 10px;
  }

  ._some-block > h4 {
    font-size: 1.3rem;
    color: #fff;
    line-height: 0;
    display: inline-block;
    margin-top: -10px;
  }

  ._some-block > .blue {
    color: #30a9de;
  }

  @media screen and (min-width: 60em) {
    ._some-block {
      margin-right: 6rem;
      margin-top: 3rem;
      margin-bottom: 1rem;
    }

    ._some-block > i {
      padding-right: 0;
      font-size: 2rem;
      line-height: 2rem;
      margin-bottom: 4rem;
    }

    ._some-block > h4 {
      display: block;
      font-size: 2rem;
    }
  }
</style>

<svelte:head>
  <title>evilfactorylabs.org - Etos</title>
  <link
    href="https://cdn.lineicons.com/1.0.1/LineIcons.min.css"
    rel="stylesheet" />
</svelte:head>

<Transition>
  <Container>
    <h2 class="o-cta__title u-mb-sm" in:fade={{ duration: 1000, delay: 500 }}>
      Ethos
    </h2>
    <div in:fade={{ duration: 1000, delay: 1000 }}>
      <Hero>
        <p class="u-mb-sm u-fs-md u-fs-sm--xs">
          <strong>etos</strong>
          /étos/ n pandangan hidup yang khas dari suatu golongan sosial;
        </p>

        <p class="u-mb-sm u-fs-md u-fs-sm--xs">
          <strong>-- kebudayaan</strong>
          sifat, nilai, dan adat-istiadat khas yang memberi watak kepada
          kebudayaan suatu golongan sosial dalam masyarakat;
        </p>
        <p class="u-mb-sm u-fs-md u-fs-sm--xs">
          <strong>-- kerja</strong>
          semangat kerja yang menjadi ciri khas dan keyakinan seseorang atau
          suatu kelompok
        </p>

        <div class="_some-block">
          <i class="lni-bulb" />
          <h4 class="u-ff-serif">Enlight</h4>
        </div>

        <div class="_some-block">
          <i class="lni-brick blue" />
          <h4 class="u-ff-serif">Valiant</h4>
        </div>

        <div class="_some-block">
          <i class="lni-sprout" />
          <h4 class="u-ff-serif">Inspire</h4>
        </div>

        <div class="_some-block">
          <i class="lni-infinite" />
          <h4 class="u-ff-serif">Loop</h4>
        </div>

      </Hero>
    </div>
  </Container>
</Transition>
