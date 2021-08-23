<script lang="ts">
  export let texto: string;
  export let duplo: boolean = false;
  export let triplo: boolean = false;
  export let operacao: boolean = false;
  export let destaque: boolean = false;
  export let onClick: (valor: string) => void = () => {};
</script>

<button
  class="botao"
  on:click={() => onClick(texto)}
  class:duplo
  class:triplo
  class:operacao
  class:destaque
>
  {texto}
</button>

<style>
  .botao {
    margin: 0;
    border-radius: 15px;
    border: 1px solid var(--cor-fundo);
    flex-basis: 25%;
    color: white;
    background-color: #444;
  }

  .duplo {
    border-radius: 15px;
    flex-basis: 50%;
  }

  .triplo {
    border-radius: 15px;
    flex-basis: 75%;
  }

  .operacao {
    background-color: purple;
    color: white;
  }

  .destaque {
    background-color: #666;
    color: white;
  }
</style>
