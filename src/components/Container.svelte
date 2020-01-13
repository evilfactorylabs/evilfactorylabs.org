<style>
  .c-container {
    width: 100%;
    height: 100vh;
    display: table;
    margin-top: 4rem;
  }

  .c-content {
    padding: 1rem 2rem;
    display: table-cell;
    vertical-align: middle;
  }

  @media screen and (min-width: 60em) {
    .c-content {
      padding: 1.8rem 5rem;
    }
  }
</style>

<div class="c-container">
  <div class="c-content">
    <slot />
  </div>
</div>
