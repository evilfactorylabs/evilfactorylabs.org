<style>
  .c-navbar {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    font-family: var(--sans-serif-font);
    font-weight: bold;
    padding: 2rem 2rem;
    padding-top: 3rem;
  }

  .c-navbar__left {
    float: left;
    width: 30%;
    margin: auto;
    text-align: center;
  }

  .c-navbar__right {
    float: left;
    width: 70%;
    text-align: right;
  }

  .c-navbar__link {
    display: inline-block;
    padding-left: 0.8rem;
    margin-bottom: 1rem;
    text-transform: uppercase;
    text-decoration: none;
  }

  .c-navbar__link:hover {
    color: var(--primary-color);
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
    <a class="c-navbar__link" href="/tentang">Tentang</a>
    <a class="c-navbar__link" href="/etos">Etos</a>
    <a class="c-navbar__link" href="/kiprah">Kiprah</a>
    <a class="c-navbar__link" href="/dukungan">Dukung(an)</a>
  </div>
</nav>
