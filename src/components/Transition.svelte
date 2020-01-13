<script>
  import { onMount } from 'svelte'
  import { fade } from 'svelte/transition'

  let isMounted = false

  onMount(() => {
    isMounted = true
  })
</script>

{#if isMounted}
  <div transition:fade={{ duration: 500 }}>
    <slot />
  </div>
{/if}
