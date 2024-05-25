<template>
    <navbar />
    <main class="p-10 min-h-screen scroll-smooth">
        <section class="h-screen flex p-10">
            <div class="mx-auto my-auto">
                <h1 class="text-5xl mb-2">Lorem impsum dolor sit amet</h1>
                <p class="w-[500px]">Lorem ipsum dolor sit amet consectetur adipisicing elit. Autem, praesentium
                    obcaecati sunt, at rerum accusamus distinctio laudantium fugiat, nesciunt magnam enim reiciendis.
                    Repellat iusto iure nemo quia impedit repellendus doloremque.</p>
            </div>
            <nuxt-link to="/quiz"
                class="mx-auto my-auto bg-emerald-600 rounded-full w-96 h-96 text-8xl flex jersey transition-colors duration-300 hover:bg-red-600 hover:text-white">
                <p class="my-auto mx-auto jersey">Jogar</p>
            </nuxt-link>
        </section>
        <section class="flex flex-col px-20" id="sobre">
            <h1 class="text-5xl mb-2">Sobre o projeto</h1>
            <p class="">Lorem ipsum dolor sit, amet consectetur adipisicing elit. Asperiores doloremque, officiis
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