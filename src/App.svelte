<script>
  import Title from "./lib/Title.svelte";
  import Description from "./lib/Description.svelte";
</script>

<div class="container">
  <h1>CFP Character Counter</h1>
  <div class="inputs">
    <Title />
    <Description heading="Description" />
    <Description heading="Additional Section (Benefits to ecosystem, etc.)" />
  </div>
</div>

<style>
  .container {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: flex-start;
    @media only screen and (max-width: 600px) {
      padding: 1rem;
    }
  }
  .inputs {
    width: 100%;
    display: flex;
    flex-direction: column;
    gap: 1rem;
  }
  h1 {
    margin-top: 1rem;
    margin-bottom: 1rem;
    font-size: 3rem;
    align-self: center;
  }
</style>
