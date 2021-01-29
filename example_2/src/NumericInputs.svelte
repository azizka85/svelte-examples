<script lang="ts">
  let a = 1;
  let b = 2;
</script>

<style>
  input {
    vertical-align: middle;
  }
</style>

<div>
  <input type="number" bind:value={a} min=0 max=10>
  <input type="range" bind:value={a} min=0 max=10>
</div>
<div>
  <input type="number" bind:value={b} min=0 max=10>
  <input type="range" bind:value={b} min=0 max=10>
</div>
<p>{a} + {b} = {a + b}</p>
