<script lang="ts">
  let m = {
    x: 0,
    y: 0
  };

  function handleMouseMove(event: MouseEvent) {
    m.x = event.x;
    m.y = event.y;
  }
</script>

<style>
  div {
    width: 100%;
    height: 240px;
    background-color: #cccccc;    
  }
</style>

<div on:mousemove={handleMouseMove}>
  The mouse position is {m.x} x {m.y}
</div>
