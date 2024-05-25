<!-- +++++++++++++++++++++++++++++++ html ++++++++++++++++++++++++++++++++ -->
<template>
    <navbar />
    <div class="p-10">
        <h1 class="text-4xl">Hmm... então quer dizer que aceitou meu desafio?!</h1>
        <p>Pois então vou te dar uma "colher de chá", escolha um tema que acredita dominar e eu te farei perguntas!</p>
        <div>
            <nuxt-link v-for="tema in temas" :key="tema" :to="`/quiz/${tema}`" >{{tema}}</nuxt-link>
        </div>
    </div>
</template>


<!-- +++++++++++++++++++++++++++++++ js ++++++++++++++++++++++++++++++++ -->
<script>
import { temas } from '~/data/data';

export default {
    data() {
        return {
            temas
        };
    }
}
</script>


<!-- +++++++++++++++++++++++++++++++ css ++++++++++++++++++++++++++++++++ -->
<style scoped>
/* css caso queiram mudar algo */
</style>