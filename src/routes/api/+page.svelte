<script lang="ts">
  import { onMount } from "svelte";
  let dados: any;
  let cep: string = "";

  const buscarCEP = async () => {
    const response = await fetch(`https://viacep.com.br/ws/${cep}/json/`);
    dados = await response.json();
  };

  onMount(() => {
    buscarCEP();
  });
</script>

<input bind:value={cep} placeholder="Digite o CEP">
<button on:click={buscarCEP}>Buscar</button>

{#if dados}
  <h1>{dados.logradouro}</h1>
{/if}

