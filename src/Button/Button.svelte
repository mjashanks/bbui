<script>
  export let primary = false,
    secondary = false,
    blue = false,
    disabled = false,
    text = false,
    red = false,
    yellow = false,
    orange = false,
    green = false,
    purple = false,
    small = false,
    medium = false,
    wide = false,
    large = false;
</script>

<style>
  button {
    font-family: var(--font-sans);
    cursor: pointer;
    font-weight: 600;
    box-sizing: border-box;
    overflow: hidden;
    border-radius: var(--border-radius-s);
    color: var(--white);
    padding: var(--spacing-s) var(--spacing-l);
    transition: all 0.2s ease 0s;
    display: inline-flex;
    text-rendering: optimizeLegibility;
    min-width: auto;
    outline: none;
    font-feature-settings: "case" 1, "rlig" 1, "calt" 0;
    -webkit-box-align: center;
    user-select: none;
    flex-shrink: 0;
    align-items: center;
    justify-content: center;
    margin: 0;
  }

  .primary {
    border: solid 1.5px var(--ink);
    background-color: var(--ink);
  }
  button.primary:hover:not([disabled]) {
    background-color: var(--white);
    color: var(--ink);
  }
  .secondary {
    border: solid 1.5px var(--grey-7);
    background-color: white;
    color: var(--ink);
  }
  button.secondary:hover:not([disabled]) {
    background-color: var(--grey-2);
    color: var(--ink);
  }
  .blue {
    background-color: var(--blue);
    border: solid 1.5px var(--blue);
  }
  button.blue:hover:not([disabled]) {
    background-color: var(--blue-light);
    color: var(--blue);
  }
  .red {
    border: solid 1.5px var(--red);
    background-color: var(--red);
    color: white;
  }
  button.red:hover:not([disabled]) {
    background-color: var(--red-light);
    color: var(--red);
  }
  .yellow {
    border: solid 1.5px var(--yellow);
    background-color: var(--yellow);
    color: white;
  }
  button.yellow:hover:not([disabled]) {
    background-color: var(--yellow-light);
    color: var(--yellow);
  }
  .orange {
    border: solid 1.5px var(--orange);
    background-color: var(--orange);
    color: white;
  }
  button.orange:hover:not([disabled]) {
    background-color: var(--orange-light);
    color: var(--orange);
  }
  .green {
    border: solid 1.5px var(--green);
    background-color: var(--green);
    color: white;
  }
  button.green:hover:not([disabled]) {
    background-color: var(--green-light);
    color: var(--green);
  }
  .purple {
    border: solid 1.5px var(--purple);
    background-color: var(--purple);
    color: white;
  }
  button.purple:hover:not([disabled]) {
    background-color: var(--purple-light);
    color: var(--purple);
  }
  .text {
    background-color: transparent;
    color: var(--grey-7);
    border: none;
    padding: 0;
  }
  button.text:hover:not([disabled]) {
    color: var(--ink);
  }
  button.text:active:not([disabled]) {
    color: var(--blue);
  }

  .small {
    font-size: var(--font-size-xs);
    padding: var(--spacing-xs) var(--spacing-m);
  }

  .medium {
    font-size: var(--font-size-m);
    padding: var(--spacing-s) var(--spacing-l);
  }

  .large {
    font-size: var(--font-size-l);
    padding: var(--spacing-m) var(--layout-l);
  }
  .wide {
    width: 100%;
    display: flex;
  }

  button:disabled {
    background-color: var(--grey-4);
    cursor: not-allowed;
    border: solid 1.5px var(--grey-4);
    color: var(--grey-5);
  }
</style>

<button
  class:primary
  class:secondary
  class:blue
  class:red
  class:yellow
  class:orange
  class:green
  class:purple
  class:small
  class:medium
  class:wide
  class:large
  class:text
  {disabled}
  on:click|preventDefault>
  <slot />
</button>
