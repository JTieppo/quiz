<template>
    <Navbar />
    <div v-if="finalizado" class="flex">
        <div class="flex flex-col p-10 my-auto items-center mx-auto">
            <h1 v-if="pontuacao >= 4" class="text-xl xl:text-4xl text-center">Muito bem! você me venceu marujo!</h1>
            <h1 v-else class="text-xl xl:text-4xl text-center">Quase lá, mas boa tentativa, acredito que logo irá me
                vencer!</h1>
            <p class="text-xl xl:text-2xl mt-10">Sua pontuaçao: {{ pontuacao }}/5</p>
            <nuxt-link class="flex mt-2 text-white bg-teal-500 w-40 md:w-96 rounded h-12 text-center " href="/">
                <p class="mx-auto my-auto md:text-2xl">Voltar</p>
            </nuxt-link>
        </div>
    </div>
    <div v-else>
        <div class="pointer-events-none text-center xl:text-end px-20 mt-4">
            <p class="text-2xl">Pontuação: {{ pontuacao }}</p>
        </div>
        <div class="flex flex-col p-6 sm:p-14 xl:p-20">
            <h3 v-if="i == 0" class="xl:text-2xl xl:w-[600px] mb-6">
                Então quer dizer que acredita ser um especialista em {{ tema.nome }}, vamos ver do que é capaz, boa
                sorte
                marujo!!
            </h3>
            <div class="flex flex-col w-full gap-4">
                <h1 class="text-xl md:text-4xl">{{ tema.perguntas[i].pergunta }}</h1>
                <p class="text-xs lg:text-base" v-if="positivo == true">{{ tema.perguntas[i].feedbackPositivo }}</p>
                <p class="text-xs lg:text-base" v-else-if="negativo == true">{{ tema.perguntas[i].feedbackNegativo }}
                </p>
                <button :class="[
                    'rounded-lg p-2 px-4 xl:text-2xl w-full',
                    verificado && opt === tema.perguntas[i].resposta ? 'bg-green-600 text-white' :
                        verificado && opt !== tema.perguntas[i].resposta ? 'bg-red-700 text-white' :
                            'bg-teal-600 hover:bg-teal-400 text-white hover:text-black'
                ]" v-for="opt in tema.perguntas[i].options" :key="opt" @click="valida(opt)" :disabled="verificado">
                    {{ opt }}
                </button>
                <button v-if="verificado" class="mt-10" @click="proxima">Próxima</button>
                <button v-else class="mt-10 text-slate-700 opacity-50" @click="proxima" disabled>Próxima</button>
            </div>
        </div>
    </div>
</template>



<script setup>
import { ref, reactive, watch, onMounted } from 'vue';
import { useRoute } from 'vue-router';
import { temas } from '~/data/data';


const route = useRoute();
const path = route.params.tema;
const tema = temas.find(tema => tema.link === path);
const i = ref(0);
const verificado = ref(false);
const valido = ref(false);
const pontuacao = ref(0);
const negativo = ref(false)
const positivo = ref(false)
const finalizado = ref(false)


function valida(opt) {
    console.log("validando", opt);
    verificado.value = true;
    if (opt === tema.perguntas[i.value].resposta) {
        valido.value = true;
        positivo.value = true;
        pontuacao.value++;
    } else {
        negativo.value = true;
        valido.value = false;
    }
}

function proxima() {
    verificado.value = false;
    positivo.value = false;
    negativo.value = false;
    if (i.value < 4) {
        i.value++;
    } else {
        finalizado.value = true;
    }
    console.log("i value",i.value)
}



watch(() => route.params.link, (newLink) => {
    temaLink.value = newLink;
    console.log('Rota mudou para:', newLink);
    console.log('Tema encontrado:', tema.value);
});

onMounted(() => {
    console.log('Componente montado');
});
</script>
