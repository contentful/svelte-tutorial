<script>
  import { hasTax } from './state.svelte';
  let { title, description, price } = $props();
  const taxRate = 1.2;
</script>

<div class="card">
    <h2>{title}</h2>
    <p>{description}</p>
    <p>${($hasTax ? price * taxRate : price).toFixed(2)}</p>
</div>

<style>
    .card {
        border: 1px solid tomato;
        width: 500px;
        
    }
    h2 {
        font-size: 30px;
        font-weight: var(--font-weight-8);
    }
    p {
        font-weight: var(--font-weight-4);
    }
</style>
  