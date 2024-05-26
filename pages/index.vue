<template>
    <navbar />
    <main class="p-6 md:p-10 min-h-screen scroll-smooth">
        <section class="xl:h-screen flex flex-col xl:flex-row ">
            <div class="flex flex-col mx-auto xl:my-auto">
                <h1 class="text-3xl xl:text-5xl mb-2 mx-auto xl:mx-0">Que tal um quiz?</h1>
                <p class="max-w-[500px] text-xs xl:text-base text-center xl:text-start">Já se perguntou de onde vem tanto conhecimento? Ou mesmo como o adiquirimos? Não, não, espera... melhor que isso seria saber o quanto de conhecimento tem, agora sim ficou interessante, então que tal um quiz?</p>
            </div>
            <nuxt-link to="/quiz/selection"
                class="mx-auto my-10 xl:my-auto text-white bg-teal-600 rounded-full w-64 h-64 md:w-80 md:h-80 xl:w-96 xl:h-96 text-8xl flex jersey transition-colors duration-300 hover:bg-teal-300 hover:text-black">
                <p class="my-auto mx-auto jersey">Jogar</p>
            </nuxt-link>
        </section>
        <section class="flex flex-col xl:px-20 mt-20 max-w-[300px] lg:max-w-[700px] xl:max-w-[900px] mx-auto" id="sobre">
            <h1 class="text-3xl xl:text-5xl mx-auto xl:mx-0 mb-2">Sobre o projeto</h1>
            <p class="text-center xl:text-start text-xs xl:text-base">Lorem ipsum dolor sit, amet consectetur adipisicing elit. Asperiores doloremque, officiis
                labore
                nisi deserunt quia veritatis dicta natus neque nemo ab eos pariatur dolores aut tempora, odit
                eveniet
                vitae. Recusandae?</p>
        </section>
    </main>
</template>

<script>
export default {
    data() {
        return {
            mensagem: "Bem-vindo à Página Principal"
        };
    }
}
</script>

<style scoped>
@font-face {
    font-family: Jersey;
    src: url('static/fonts/Jersey10-Regular.ttf') format(truetype);
}

.jersey {
    font-family: Jersey;
}

/* css caso queiram mudar algo */
</style>