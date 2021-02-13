<script>
  import HighlightedText from "./HighlightedText.svelte";
  import Timer from "./Timer";

  let text = "Lorem ipsum dolor sit amet consectetur adipisicing elit. Rem voluptatem magni commodi magnam, molestias fugiat cum nam nisi eius dignissimos illum omnis. Voluptatem ut cumque vero quis eveniet explicabo ad!"
  let typed = "";
  let started = false;
  let finished = false;

  $: if (typed !== "") started = true;
  $: if (typed === text) finished = true;
</script>

<h1>Typing Game!</h1>
<Timer started finished/>

<h2>Please type this as fast as you can:</h2>
<HighlightedText text={text} typed={typed} />

<textarea bind:value={typed} autofocus />

<style>
h1 {
  font-size: 400%;
}
h2 {
  font-size: 200%;
}
textarea {
  width: 100%;
  min-height: 200px;
}
</style>
