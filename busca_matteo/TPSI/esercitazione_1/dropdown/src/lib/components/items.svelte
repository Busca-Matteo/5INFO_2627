<script>
    export let opzioni = [];
</script>

<ul class="menu">
    {#each opzioni as op}
        <li>{op}</li>        
    {/each}
</ul>

<style>
    .menu {
        list-style: none;
        padding: 10px;
        margin: 5px 0 0 0;
        border: 1px solid #ccc;
        border-radius: 8px;
        background-color: white;
    }
    li {
        padding: 5px 10px;
    }
</style>