<script>
  import { extraSections } from "./store";
  function addSection() {
    $extraSections = [...$extraSections, { id: Date.now(), value: "" }];
  }
</script>

<div>
  <button on:click={addSection}>Add Section</button>
</div>

<style>
  :global(button) {
    background-color: rgb(173, 133, 86);
    color: #fafafa;
    border: none;
    border-radius: 0.7rem;
    padding: 1rem;
    text-decoration: none;
    display: inline-block;
    font-size: 0.9rem;
  }
  :global(button:hover) {
    background-color: rgb(173, 133, 86, 0.9);
  }
</style>
