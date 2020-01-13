<script>
  /**
   * This code was taken from https://github.com/henriquehbr/svelte-typewriter
   * as a hotfix
   *
   * Author: henriquehbr
   * License: MIT
   */

  import { onMount } from 'svelte'
  export let interval = 30
  export let cascade = false
  export let loop = false
  export let cursor = true
  if (cascade && loop)
    throw new Error('`cascade` mode should not be used with `loop`!')
  const sleep = ms => new Promise(resolve => setTimeout(resolve, ms))
  const rng = (min, max) => Math.floor(Math.random() * (max - min) + min)
  const typingInterval = async () =>
    Array.isArray(interval)
      ? await sleep(interval[rng(0, interval.length)])
      : await sleep(interval)
  const typewriterEffect = async (
    el,
    { loopAnimation } = { loopAnimation: false }
  ) => {
    const elText = el.textContent.split('')
    el.textContent = ''
    el.classList.add('typing')
    for (const letter of elText) {
      el.textContent += letter
      const fullyWritten = loopAnimation && el.textContent === elText.join('')
      if (fullyWritten) {
        typeof loop === 'number' ? await sleep(loop) : await sleep(1500)
        while (el.textContent !== '') {
          el.textContent = el.textContent.slice(0, -1)
          await typingInterval()
        }
        return
      }
      await typingInterval()
    }
    if (el.nextSibling !== null) el.classList.remove('typing')
  }
  let node
  onMount(async () => {
    const elements = [...node.children].map(el =>
      loop ? el.textContent.split('') : { el, text: el.textContent.split('') }
    )
    if (cascade) {
      elements.forEach(({ el }) => (el.textContent = ''))
      for (const { el, text } of elements) {
        el.textContent = text.join('')
        await typewriterEffect(el)
      }
    } else if (loop) {
      const loopParagraphTag = node.firstChild.tagName.toLowerCase()
      const loopParagraph = document.createElement(loopParagraphTag)
      node.childNodes.forEach(el => el.remove())
      node.appendChild(loopParagraph)
      while (true) {
        for (const text of elements) {
          loopParagraph.textContent = text.join('')
          await typewriterEffect(loopParagraph, { loopAnimation: true })
        }
      }
    } else {
      const hasSingleTextNode = el =>
        el.childNodes.length === 1 && el.childNodes[0].nodeType === 3
      hasSingleTextNode(node)
        ? typewriterEffect(node)
        : elements.forEach(({ el }) => typewriterEffect(el))
    }
  })
</script>

<style>
  @keyframes cursorFade {
    0% {
      opacity: 1;
    }
    50% {
      opacity: 0;
    }
    100% {
      opacity: 1;
    }
  }
  .cursor :global(.typing::after) {
    content: '▌';
    color: var(--cursor-color);
    animation: cursorFade 1.25s infinite;
  }
</style>

<div
  class:cursor
  style="--cursor-color: {typeof cursor === 'string' ? cursor : 'black'}"
  bind:this={node}>
  <slot />
</div>
