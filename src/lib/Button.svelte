<script>
  import Description from "./Description.svelte";
  function addSection() {
    const newSection = new Description({
      target: document.getElementById("inputs"),
      props: {
        heading: "Additional Section",
      },
    });
  }
</script>

<div>
  <button on:click={addSection}>Add Section</button>
</div>

<style>
  button {
    background-color: rgb(173, 133, 86);
    color: #fafafa;
    border: none;
    border-radius: 0.7rem;
    padding: 1rem;
    text-decoration: none;
    display: inline-block;
    font-size: 0.9rem;
  }
  button:hover {
    background-color: rgb(173, 133, 86, 0.9);
  }
</style>
