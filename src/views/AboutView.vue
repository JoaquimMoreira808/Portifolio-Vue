<template>
  <div>
    <BackButton />
    <div class="text-white px-4 py-12 max-w-5xl mx-auto">
      <h1 class="text-5xl font-bold text-center mb-12">Sobre Mim</h1>

      <section class="mb-16">
        <h2 class="text-3xl font-semibold mb-4 text-center">Jornada</h2>
        <p class="text-center text-lg max-w-3xl mx-auto">
          Quando iniciei na programção, não sabia nem por onde começar. Tudo era novo, confuso e até um pouco assustador. Mas com o tempo, estudo e prática, fui me apaixonando por programação. Errando, acertando, fui crescendo. Hoje, olho pra trás com orgulho e vejo o quanto evoluí — ainda tenho muito a aprender, mas já me tornei alguém que ama codar e busca sempre ir além.
        </p>
      </section>

      <section class="mb-16">
        <h2 class="text-3xl font-semibold mb-8 text-center">Projetos</h2>
        <div class="flex flex-col md:flex-row justify-center items-center gap-8">
          <CardComponent
            :img="PhpLogo"
            alt="Projeto 1"
            @click="abrirProjeto('https://github.com/JoaquimMoreira808/CrudPHP')"
          />
          <CardComponent
            :img="CsharpLogo"
            alt="Projeto 2"
            @click="abrirProjeto('https://github.com/JoaquimMoreira808/LocacaoCsharp')"
          />
          <CardComponent
            :img="PythonLogo"
            alt="Projeto 3"
            @click="abrirProjeto('https://github.com/JoaquimMoreira808/Jogo')"
          />
        </div>
      </section>

      <section>
        <h2 class="text-3xl font-semibold mb-4 text-center">Curiosidades</h2>
        <p class="text-center text-lg max-w-3xl mx-auto">
          Já desenvolvi alguns projetos que mostram bem minha evolução como dev: um CRUD completo em PHP, um sistema de locação com interface em C#, e um jogo em Python com elementos interativos. Cada um me ensinou muito sobre lógica, estrutura e boas práticas.
        </p>
      </section>
    </div>
  </div>
</template>


<script>
import CardComponent from '@/components/CardComponent.vue'
import BackButton from '@/components/BackButtonComponent.vue'
import PythonLogo from '@/imgs/PythonLogo.webp'
import PhpLogo from '@/imgs/PhpLogo.png'
import CsharpLogo from '@/imgs/CsharpLogo.webp'

export default {
  name: 'AboutView',
  components: { CardComponent, BackButton },
  data() {
    return {
      PhpLogo,
      PythonLogo,
      CsharpLogo
    }
  },
  methods: {
    abrirProjeto(link) {
      window.open(link, '_blank')
    }
  }
}
</script>