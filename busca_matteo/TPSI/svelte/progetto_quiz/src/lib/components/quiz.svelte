<script>
    import { domanda } from "#lib/domande.js";

    let n_d = 0;
    let risposta = false
</script>

<h2>sei alla domanda {n_d} di 6</h2>
<progress max="6" value="0">{n_d}</progress>

<h2>{domanda.keys()}</h2>