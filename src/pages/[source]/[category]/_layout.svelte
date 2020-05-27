<script>
  import { url } from '@sveltech/routify'
  import { writable } from 'svelte/store';
  import Transition from "../../../components/Transition.svelte"
  const width = writable();
</script>

<style>
  a {
    display: block;
    width: 100%;
  }
</style>

<a href={$url("/")}>&larr; A Casa</a>
<a href={$url("../")}>&larr; Categoria</a>
<div bind:offsetWidth={$width}>
  <slot decorator={Transition} scoped={{ width }} />
</div>
