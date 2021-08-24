<script lang="ts">
  export let valor: string;

  $: tamanhoFonte = valor.length > 20 ? "pequena" : `s-${valor.length}`;
</script>

<div class={`tela ${tamanhoFonte}`}>
  <span>{valor}</span>
</div>

<style>
  .tela {
    display: flex;
    flex: 1;
    justify-content: flex-end;
    align-items: center;
    padding: 0px 5px;
    font-size: 3.4rem;
    color: white;
    overflow: hidden;
    margin: 2px 1px;
  }

  .s-10 {
    font-size: 3.3rem;
  }
  .s-11 {
    font-size: 3rem;
  }
  .s-12 {
    font-size: 2.8rem;
  }
  .s-13 {
    font-size: 2.6rem;
  }
  .s-14 {
    font-size: 2.44rem;
  }
  .s-15 {
    font-size: 2.3rem;
  }
  .s-16 {
    font-size: 2.16rem;
  }
  .s-17 {
    font-size: 2.04rem;
  }
  .s-18 {
    font-size: 1.96rem;
  }
  .s-19 {
    font-size: 1.86rem;
  }
  .s-20 {
    font-size: 1.78rem;
  }

  .pequena {
    font-size: 1.5rem;
  }
</style>
