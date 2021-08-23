<script lang="ts">
  import Botao from "./Botao.svelte";
  import Linha from "./Linha.svelte";
  import Tela from "./Tela.svelte";

  let valor = "0";

  function numeroDigitaro(numero: string) {
    valor += numero;
  }
</script>

<div class="calculadora">
  <Tela {valor} />
  <Linha>
    <Botao destaque triplo texto="AC" />
    <Botao operacao texto="/" />
  </Linha>
  <Linha>
    <Botao texto="7" onClick={numeroDigitaro} />
    <Botao texto="8" onClick={numeroDigitaro} />
    <Botao texto="9" onClick={numeroDigitaro} />
    <Botao operacao texto="*" />
  </Linha>
  <Linha>
    <Botao texto="4" />
    <Botao texto="5" />
    <Botao texto="6" />
    <Botao operacao texto="+" />
  </Linha>
  <Linha>
    <Botao texto="1" />
    <Botao texto="2" />
    <Botao texto="3" />
    <Botao operacao texto="-" />
  </Linha>
  <Linha>
    <Botao duplo texto="0" />
    <Botao texto="," />
    <Botao operacao texto="=" />
  </Linha>
</div>

<style>
  .calculadora {
    background-color: var(--cor-fundo);
    height: 250px;
    width: 160px;
    padding: 10px;
    border-radius: 10px;

    display: flex;
    flex-direction: column;
  }
</style>
