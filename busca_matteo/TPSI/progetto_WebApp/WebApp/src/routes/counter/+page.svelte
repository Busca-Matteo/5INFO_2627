<script>
    import Counter from "../../lib/components/counter.svelte";
    import DB_Counter from "../../lib/components/double_counter.svelte";
    let contatore = 0;
    let contatore_db = 0;
    let numeri = [1,2,3,4,5,6,7,8,9,10];
    let sottolineato = true;
    $: doppio = contatore * 2;
    $: {sottolineato = contatore == 7 ? false : true}   


    function gestici_evento(evento){
        alert(`${evento.detail.tipo} a ${evento.detail.valore}`);
    }
</script>

<h1>Counter</h1>

<h2 class:sottolineato>il valore del contatore: {contatore}</h2>


<Counter bind:counter={contatore} on:contatore={gestici_evento}/>

<h2 class:rosso="{contatore_db < 5}">Il valore del contatore vale: {contatore_db}</h2>

<DB_Counter bind:counter_db={contatore_db} on:contatore={gestici_evento}/>

<h2> il suo  doppio vale: {doppio}</h2>

<ul>
    {#each numeri as numero}
        <li>numeri[]:{numero}</li>
    {/each}     
</ul>


<style>
    .rosso{ color: red;}
    .verde{ color: green;}
    .sottolineato{ text-decoration: underline;}
</style>