<script>
    import Counter from "../../lib/components/counter.svelte";
    import DB_Counter from "../../lib/components/double_counter.svelte";
    let contatore = 0;
    let contatore_db = 0;
</script>

<h1>Counter</h1>

<h2>il valore del contatore è: {contatore}</h2>
<Counter bind:counter={contatore}/>

<h2>il valore del Double contatore è: {contatore_db}</h2>
<DB_Counter bind:counter={contatore_db}/>