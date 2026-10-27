<script>
    export let categoria = 'nome'
</script>

<button> {categoria} </button>

<style>
    button{
        background-color: red;
        border-radius: 15px;
        border: 0px;
        width: 200px;
        height: 50px;
        color: white;
        text-decoration: solid;
        font-size: 20px;
        text-transform: capitalize;
    }
    button:hover{
        background-color: darkred;
    }
</style>

