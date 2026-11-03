<script>
    import Items from "./items.svelte";   
    export let categoria = 'nome';
    export let lista = [];
    export let active = '';
</script>

<div>
    <button on:click={() => active = (active === categoria ? '' : categoria)}>
        {categoria}
    </button>

    {#if active === categoria}
        <Items opzioni={lista} />
    {/if}
</div>

<style>
    div {
        margin-right: 15px;
    }
    button {
        background-color: red;
        border-radius: 15px;
        border: 0px;
        width: 200px;
        height: 50px;
        color: white;
        font-size: 20px;
        text-transform: capitalize;
        font-weight: bolder;
    }
    button:hover {
        background-color: darkred;
    }
</style>
