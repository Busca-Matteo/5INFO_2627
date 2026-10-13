<script>
    let nome,cognome,eta;
</script>

<h1> Input page</h1>

Nome <input bind:value={nome}>
Cognome<input bind:value={cognome}>
Età <input bind:value={eta}>

<br><br>

Io sono {nome} {cognome} e ho {eta}.

