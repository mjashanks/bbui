<script>
  export let forAttr = "",
    extraSmall = false,
    small = false,
    medium = false,
    large = false,
    extraLarge = false,
    white = false,
    grey = false,
    black = false;
</script>

<style>
  .bb-label {
    font-family: var(--font-sans);
    font-weight: 500;
    text-rendering: var(--text-render);
    color: var(--ink);
    font-size: var(--font-size-s);
    margin-bottom: 12px;
    display: block;
    line-height: 1.5;
  }

  .extraSmall {
    font-size: var(--font-size-xs);
  }

  .small {
    font-size: var(--font-size-s);
  }

  .medium {
    font-size: var(--font-size-m);
  }

  .large {
    font-size: var(--font-size-l);
  }

  .extraLarge {
    font-size: var(--font-size-xl);
  }

  .white {
    color: var(--white);
  }

  .grey {
    color: var(--grey-5);
  }

  .black {
    color: var(--ink);
  }
</style>

<label
  class="bb-label"
  class:extraSmall
  class:small
  class:medium
  class:large
  class:extraLarge
  class:white
  class:grey
  class:black
  for={forAttr}>
  <slot />
</label>
