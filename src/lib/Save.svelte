<script>
  import { title, description, extraSections } from "./store.js";
  function saveContents() {
    localStorage.setItem("title", $title);
    localStorage.setItem("description", $description);
    localStorage.setItem("extraSections", JSON.stringify($extraSections));
    console.log(JSON.stringify($extraSections));
  }
</script>

<div>
  <button on:click={saveContents}>Save</button>
</div>
