<script lang="ts">
  import { createEventDispatcher } from 'svelte';

  const dispatch = createEventDispatcher<{message: {text: string}}>();
  const anyDispatch = createEventDispatcher();

  function sayHello() {
    dispatch('message', {
      text: 'Hello!'
    });
    anyDispatch('anyMessage', {
      time: new Date()
    });
  }
</script>

<button on:click={sayHello}>
  Click to say hello
</button>
