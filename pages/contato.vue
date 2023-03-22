<template>
    <h1> Página de Contato </h1>
    <FormContato 
        @enviarDados = "receberDados"
    />
    <hr>
        <p> Lista de Contatos: </p>
        <ul v-for="ct in Object.keys(listaContato)">
            <li> Nome: <strong> {{  listaContato[ct].nome }} </strong></li>
            <li> Email: <strong> {{  listaContato[ct].email }} </strong></li>
            <li> Mensagem: <strong> {{  listaContato[ct].msg }} </strong></li>
            <hr>
        </ul>
</template>

<script>
    export default {
        data() {
            return {
                listaContato: []
            }
        },
        methods: {
            receberDados(dados) {
                this.listaContato.push(dados)
            }
        }
    }
</script>