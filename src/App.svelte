<script lang="ts">
  import Calculadora from "./components/Calculadora.svelte";
</script>

<main>
  <Calculadora />
</main>

<style>
  :global(body) {
    background-color: #222;
  }

  :root {
    --cor-fundo: black;
  }

  main {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
  }
</style>
