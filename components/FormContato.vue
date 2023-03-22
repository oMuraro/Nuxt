<template>
    <form action="" @submit.prevent = "receberDados">
        <label for="nome">Nome: </label>
        <input v-model="inputNome" type="text"  name="nome" id="nome">
        <label for="email">Email: </label>
        <input v-model="inputEmail" type="text" name="email" id="email">

        <label for="msg">Mensagem: </label>
        <textarea v-model="inputMensagem" name="mensagem" id="msg"></textarea>

        <button>Enviar</button>
    </form>
</template>

<script>

    export default {
        data() {
            return {
                inputNome: "",
                inputEmail: "",
                inputMensagem: ""
            }
        },
        methods: {
            receberDados() {
                const dados = {
                    nome: this.inputNome,
                    email: this.inputEmail,
                    msg: this.inputMensagem,
                }
                this.$emit("enviarDados", dados)
            }
        }
    }
</script>