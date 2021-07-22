<template>
    <div>
        <h1 class="display-3 font-weight-light mb-4">
            Negocie e Consulte sua Ações
        </h1>
        <v-sheet :elevation="6" class="pa-2 primary">
            <v-icon class="white--text mr-3 font-weight-light">info</v-icon>
            <span>Você pode Salvar & Carregar os Dados</span>
        </v-sheet>
        <v-sheet :elevation="6" class="pa-2 success darken-1 mt-3">
            <v-icon class="white--text mr-3 font-weight-light">info</v-icon>
            <span>Clique em 'Finalizar Dia' para iniciar um novo dia!</span>
        </v-sheet>
        <v-divider class="my-4"></v-divider>
        <p class="display-1"><strong>Seu saldo:</strong> {{ funds | currency}}</p>
    </div>
</template>

<script>
export default {
    name: 'home',
    computed: {
        funds() {
            return this.$store.getters.funds
        }
    }
};
</script>

<style>
</style>