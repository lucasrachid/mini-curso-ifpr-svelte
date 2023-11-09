<script lang="ts">
    let contador  = 0;
</script>

<h1>{contador}</h1>
<input type="text">
<button on:click={()=> contador++}>Aumentar</button>
<button on:click={()=> contador--}>Diminuir</button>
