<script>
  let count = $state(0)
  const increment = () => {
    count += 1
  }
</script>

<button class="button" onclick={increment}>
  count is {count}
</button>

<style>
  .button{
    border-color: red;
  }
</style>
