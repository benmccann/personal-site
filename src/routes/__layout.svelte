<script>
  // import Prism from 'prismjs'
  import { page } from '$app/stores'
  import './base.css'
  import Header from '$lib/Header.svelte'
  import Footer from '$lib/Footer.svelte'
  // import { onMount } from 'svelte'

  // onMount(() => Prism.highlightAll())
</script>

{#if $page.url.pathname !== '/'}
  <div id="dots">
    <img src="/images/dots.svg" alt="A decorative dot grid">
  </div>
  <Header title={'Jacob Stordahl'} />
{/if}
  <main>
    <slot />
  </main>
<Footer />

<style>
  #dots {
    display: none;
  }
  main {
    padding: 1rem;
    margin: auto;
    width: clamp(300px, calc(80vw + 5px), 1220px);
  }
</style>
