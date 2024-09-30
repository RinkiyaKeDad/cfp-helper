<script>
  import Title from "./lib/Title.svelte";
  import Description from "./lib/Description.svelte";
  import AddSection from "./lib/AddSection.svelte";
  import Save from "./lib/Save.svelte";
  import Clear from "./lib/Clear.svelte";
  import { description, extraSections } from "./lib/store";
  import { onMount } from "svelte";

  onMount(() => {
    if (localStorage.getItem("extraSections") != null) {
      $extraSections = JSON.parse(localStorage.getItem("extraSections"));
    }
    $description = localStorage.getItem("description");
    console.log(JSON.parse(localStorage.getItem("extraSections")));
  });
</script>

<div class="container">
  <h1>CFP Character Counter</h1>
  <div class="inputs" id="inputs">
    <Title />
    <Description bind:text={$description} />
    {#each $extraSections as section (section.id)}
      <Description heading="Additional Section" bind:text={section.value} />
    {/each}
  </div>
  <div class="btns">
    <AddSection />
    <Save />
    <Clear />
  </div>
</div>

<style>
  .container {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: flex-start;
    margin-bottom: 5rem;
    @media only screen and (max-width: 600px) {
      padding: 1rem;
    }
  }
  .inputs {
    width: 100%;
    display: flex;
    flex-direction: column;
    gap: 1rem;
    margin-bottom: 1rem;
  }
  .btns {
    display: flex;
    gap: 1rem;
  }
  h1 {
    margin-top: 1rem;
    margin-bottom: 1rem;
    font-size: 3rem;
    align-self: center;
  }
</style>
