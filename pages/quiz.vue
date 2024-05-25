<!-- +++++++++++++++++++++++++++++++ html ++++++++++++++++++++++++++++++++ -->
<template>
    <div>
        <navbar/>
        <h1>Página quiz</h1>
        <nuxt-link to="/">Início</nuxt-link>
    </div>
</template>


<!-- +++++++++++++++++++++++++++++++ js ++++++++++++++++++++++++++++++++ -->
<script>
export default {
    data() {
        return {
            mensagem: "Bem-vindo à Página Principal"
        };
    }
}
</script>


<!-- +++++++++++++++++++++++++++++++ css ++++++++++++++++++++++++++++++++ -->
<style scoped>
    /* css caso queiram mudar algo */
</style>