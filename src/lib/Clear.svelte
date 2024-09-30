<script>
  import { title, description, extraSections } from "./store.js";
  function saveContents() {
    $title = "";
    $description = "";
    $extraSections = [];
    localStorage.clear();
  }
</script>

<div>
  <button on:click={saveContents}>Clear</button>
</div>
