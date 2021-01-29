<script lang="ts">
  function sleep(ms: number) {
    return new Promise(resolve => setTimeout(resolve, ms));
  }  

  async function getRandomNumber(max: number) {
    await sleep(3000);
    return max * Math.random();
  }

  let promise = getRandomNumber(100);

  function handleClick() {
    promise = getRandomNumber(100);
  }
</script>

<button on:click={handleClick}>
  generate random number
</button>

{#await promise}
  <p>... waiting</p>
{:then number}
  <p>The number is {number.toFixed(0)}</p>
{:catch error}
  <p style="color: red">{error?.message}</p>
{/await}
