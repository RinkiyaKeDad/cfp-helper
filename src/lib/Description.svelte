<script>
  let count = 0;
  let words = 0;
  function handleKeyUp() {
    count = text.length;
    words = text.trim().split(/\s+/).length;
    if (text.length == 0) {
      words = 0;
    }
  }
  $: text, handleKeyUp();
  export let text = "";
  export let heading = "Description";
</script>

<div>
  <label for="title">{heading}</label>
  <textarea id="description" name="description" bind:value={text}></textarea>
  <p>Characters: {count}</p>
  <p>Words: {words}</p>
</div>

<style>
  div {
    display: flex;
    flex-direction: column;
  }
  textarea {
    resize: none;
    min-width: 100%;
    min-height: 15rem;
    padding: 0.35rem;
    font-size: 1rem;
    border: 1px solid #ccc;
    border-radius: 5px;
    margin-bottom: 0.3rem;
  }
</style>
