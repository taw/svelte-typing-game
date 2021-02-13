<script>
  export let text;
  export let typed;
</script>

<style>
  .red {
    color: red;
  }
  .green {
    color: green;
  }
</style>

<div>
  {#each text as letter, i}
    <span
      class:green={typed[i] === letter}
      class:red={typed[i] && typed[i] !== letter}
    >{letter}</span>
  {/each}
</div>
