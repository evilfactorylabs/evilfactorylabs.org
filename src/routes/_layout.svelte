<script>
  import Navbar from '../components/Navbar'

  export let segment
</script>

<main>
  <slot />
  <Navbar {segment} />
</main>
