<script>
  export let started;
  export let finished;
  let time = 0;

  setInterval(() => {
    if (started && !finished) {
      time += 1;
    }
  }, 1000);
</script>

{#if started}
  {#if finished}
    <div>
      You finished in {time}s
    </div>
  {:else}
    <div>
      So far: {time}s
    </div>
  {/if}
{/if}
