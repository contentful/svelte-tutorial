<script>
  import { hasTax } from './state.svelte';

  const toggle = () => {
    $hasTax = !$hasTax;
  }
</script>

<div>
  <button class="button" on:click={toggle}>
    Toggle Tax: {$hasTax ? "ON" : "OFF"}
  </button>
</div>

<style>
  .button{
    border-color: blue;
  }
</style>
