<script>
  let someText = `Frontend Developer`;
  let count = 0;
  function handleClick() {
    count = count+1;
  }
</script>

<div class="About">
  <p>
    {someText}
  </p>
  <button on:click={handleClick}>Click {count === 0 ? '' : count} </button>
</div>

<style>
  p {
    color: var( --theme-color);
    font-size: 22px;
  }
</style>