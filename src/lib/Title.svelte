<script>
  let title = "";
</script>

<div>
  <label for="title">Title</label>
  <input type="text" id="title" name="title" bind:value={title} />
</div>

<style>
  div {
    display: flex;
    flex-direction: column;
  }
  :global(label) {
    font-size: 1.5rem;
  }
  input {
    min-width: 100%;
    padding: 0.35rem;
    font-size: 1rem;
    text-transform: capitalize;
    border: 1px solid #ccc;
    border-radius: 5px;
  }
</style>
