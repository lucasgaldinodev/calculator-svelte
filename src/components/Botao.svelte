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
    border-radius: 50px;
    border: 3px solid var(--cor-fundo);
    flex-basis: 25%;
    color: white;
    background-color: #444;
    font-size: 2.3rem;
  }

  .botao:hover {
    background-color: #555;
  }

  .duplo {
    flex-basis: 50%;
  }

  .triplo {
    flex-basis: 75%;
  }

  .operacao {
    background-color: purple;
    color: white;
  }

  .operacao:hover {
    background-color: #909;
  }

  .destaque {
    background-color: #666;
    color: white;
  }

  .destaque:hover {
    background-color: #777;
  }
</style>
