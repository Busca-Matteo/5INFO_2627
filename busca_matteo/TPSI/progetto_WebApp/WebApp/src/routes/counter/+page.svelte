<script>
    import Counter from "../../lib/components/counter.svelte";
    import DB_Counter from "../../lib/components/double_counter.svelte";
    let contatore = 0;
    let contatore_db = 0;
    let numeri = [1,2,3,4,5,6,7,8,9,10]
</script>

<h1>Counter</h1>

{#if contatore < 5}
    <h2 class="rosso">il valore del contatore: {contatore}</h2>
{:else}
    <h2 class="verde">il valore del contatore: {contatore}</h2>
{/if}

<Counter bind:counter={contatore}/>

{#if contatore_db < 5}
    <h2 class="rosso">il valore del contatore: {contatore_db}</h2>
{:else}
    <h2 class="verde">il valore del contatore: {contatore_db}</h2>
{/if}

<DB_Counter bind:counter={contatore_db}/>

<ul>
    {#each numeri as numero}
        <li>numeri[]:{numero}</li>
    {/each}     
</ul>


<style>
    .rosso{ color: red;}
    .verde{ color: green;}
</style>