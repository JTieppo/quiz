<!-- +++++++++++++++++++++++++++++++ html ++++++++++++++++++++++++++++++++ -->
<template>
    <navbar />
    <div class="flex flex-col p-20">
        <h1 class="self-center text-4xl">Hmm... então quer dizer que aceitou meu desafio?!</h1>
        <p class="self-center">Pois então vou te dar uma "colher de chá", escolha um tema que acredita dominar e eu te farei perguntas!</p>
        <div class="grid grid-flow-row grid-cols-4 gap-4 mt-10">
            <nuxt-link class="bg-teal-600 hover:bg-teal-400 text-white hover:text-black rounded-lg p-2 px-4 text-2xl h-12" v-for="tema in temas" :key="tema" :to="`/quiz/dynamic/${tema.link}`" >{{tema.nome}}</nuxt-link>
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