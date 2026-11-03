<script>
    import DropDown from "#lib/components/drop_down.svelte";
    
    const Regioni = ["Piemonte", "Lombardia", "Lazio", "Liguria", "Puglia"];
    const Città = ["Torino", "Milano", "Roma", "Genova"];
    const Stato = ["Italia", "Francia", "Germania", "Olanda"];

    let activeDropdown = ''; 
</script>

<div class="container">
    <DropDown 
        categoria="Regioni" 
        listaOpzioni={Regioni} 
        bind:active={activeDropdown}
    />

    <DropDown 
        categoria="Città" 
        listaOpzioni={Città} 
        bind:active={activeDropdown}
    />

    <DropDown 
        categoria="Stato" 
        listaOpzioni={Stato} 
        bind:active={activeDropdown}
    />
</div>
