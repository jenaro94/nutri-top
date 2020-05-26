<script>
  import { scale, fly } from 'svelte/transition'
  import { BaseTransition } from "@sveltech/routify/decorators"
  export let scoped
  const { width } = scoped
  const configs = [
    {
      condition: ({ routes }) => routes[0] === routes[1],
      transition: () => {},
    },
    {
      condition: c => c.toDescendant,
      transition: fly,
      inParams: { x: $width, duration: 500 },
      outParams: { x: -$width, duration: 500 },
    },
    {
      condition: c => c.toAncestor,
      transition: fly,
      inParams: { x: -$width, duration: 500 },
      outParams: { x: $width, duration: 500 },
    },
    {
      // No matching config. We don't want a transition
      condition: () => true,
      transition: () => {},
    },
  ]
</script>

<BaseTransition {configs}>
  <slot />
</BaseTransition>
