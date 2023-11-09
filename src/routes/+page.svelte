<script lang="ts">
    const nome = "Rachid";
    let contador = 0;

    let soma = () => {
        contador += contador;
    }

    let subtracao = () => {
        contador -= contador;
    }

</script>

<h1>Olá {nome}</h1>
<h2>{contador}</h2>
<button on:click={() => contador++}>Aumentar</button>
<button on:click={() => contador --}>Diminuir</button>
