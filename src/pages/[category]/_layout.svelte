<script>
  import { url } from '@sveltech/routify'
  import { writable } from 'svelte/store';
  import Transition from "../../components/Transition.svelte"
  const width = writable();
</script>

<style>
  header {
    height: 40px;
    width: 100%;
    display: flex;
    align-items: center;
  }
</style>

<header>
  <nav>
    <a href={$url("/")}>&larr; A casa</a>
  </nav>
</header>

<main bind:offsetWidth={$width}>
  <slot decorator={Transition} scoped={{ width }} />
</main>
