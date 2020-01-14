<script>
  import { beforeUpdate } from 'svelte'

  export let segment

  let isSidebarOpen = false
  let previousSegment = null

  function toggleSidebar() {
    isSidebarOpen = !isSidebarOpen
  }

  beforeUpdate(() => {
    if (previousSegment !== segment) {
      toggleSidebar()

      if (segment === undefined || previousSegment === null) {
        isSidebarOpen = false
      }
    }

    previousSegment = segment
  })
</script>

<style>
  .c-navbar {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    font-family: var(--sans-serif-font);
    font-weight: bold;
    padding: 2rem 2rem;
    padding-top: 1.5rem;
  }

  .c-navbar__left {
    float: left;
    width: 50%;
    margin: auto;
    text-align: center;
  }

  .c-navbar__right {
    float: left;
    width: 50%;
    text-align: right;
  }

  .c-navbar__link {
    display: block;
    padding-left: 0.8rem;
    margin-bottom: 1rem;
    text-transform: uppercase;
    text-decoration: none;
    transition: 0.3s all;
    transform: translate(150px, 0);
  }

  .c-navbar__link--is-active {
    color: var(--primary-color);
  }

  .c-navbar__link--is-show {
    transform: translate(0, 0);
  }

  .c-navbar__link:hover {
    color: var(--primary-color);
  }

  .c-navbar__toggler {
    background: transparent;
    border: 0;
    color: #fff;
    font-family: inherit;
    font-size: 14px;
    margin-bottom: 2rem;
    font-weight: bold;
    text-transform: uppercase;
    letter-spacing: 2px;
    text-align: right;
  }

  ._hidden {
    display: none;
  }

  @media screen and (min-width: 60em) {
    .c-navbar {
      padding: 3rem 5rem;
      padding-top: 4rem;
    }

    .c-navbar__left {
      width: 15%;
    }

    .c-navbar__right {
      width: 85%;
    }

    .c-navbar__link {
      display: inline-block;
      letter-spacing: 2px;
      padding-left: 1.5rem;
      transform: translate(0, 0);
    }

    .c-navbar__toggler {
      display: none;
    }
  }
</style>

<nav class="c-navbar cf">
  <div class="c-navbar__left">
    <a href="/">
      <img src="/logo.png" alt="evilfactorylabs logo" width="80" />
    </a>
  </div>
  <div class="c-navbar__right">
    <button class="c-navbar__toggler" on:click={toggleSidebar}>
      {isSidebarOpen ? 'Tutup' : 'Menu'}
    </button>
    <a
      class="c-navbar__link"
      class:c-navbar__link--is-show={isSidebarOpen}
      class:c-navbar__link--is-active={segment === 'tentang'}
      href="/tentang">
      Tentang
    </a>
    <a
      class="c-navbar__link"
      class:c-navbar__link--is-show={isSidebarOpen}
      class:c-navbar__link--is-active={segment === 'etos'}
      href="/etos">
      Etos
    </a>
    <a
      class="c-navbar__link"
      class:c-navbar__link--is-show={isSidebarOpen}
      class:c-navbar__link--is-active={segment === 'kiprah'}
      href="/kiprah">
      Kiprah
    </a>
    <a
      class="c-navbar__link"
      class:c-navbar__link--is-show={isSidebarOpen}
      class:c-navbar__link--is-active={segment === 'dukungan'}
      href="/dukungan">
      Dukung(an)
    </a>
    <a href="/cerita" class="_hidden">Cerita</a>
  </div>
</nav>
