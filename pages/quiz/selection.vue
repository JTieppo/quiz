<!-- +++++++++++++++++++++++++++++++ html ++++++++++++++++++++++++++++++++ -->
<template>
    <navbar />
    <div class="flex flex-col p-10 xl:p-20">
        <div class="max-w-[400px] mx-auto xl:max-w-none ">
            <h1 class="self-center xl:text-4xl text-center xl:text-start">Hmm... então quer dizer que aceitou meu
                desafio?!</h1>
            <p class="self-center text-xs text-center">Pois então vou te dar uma "colher de chá", escolha
                um tema que acredita dominar e eu te farei perguntas!</p>
        </div>
        <div class="grid grid-flow-row grid-cols-1 md:grid-cols-2 xl:grid-cols-4 gap-4 mt-10">
            <nuxt-link
                class="bg-teal-600 hover:bg-teal-400 text-white hover:text-black rounded-lg p-2 px-4 xl:text-2xl xl:h-12"
                v-for="tema in temas" :key="tema" :to="`/quiz/dynamic/${tema.link}`">{{ tema.nome }}</nuxt-link>
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